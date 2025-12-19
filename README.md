# NLP — Travaux Pratiques (TPs)

Submitted for the **Natural Language Processing** class with **Benjamin Dallard**.

This repository contains a set of practical notebooks (TP2 → TP6) covering core NLP tooling and workflows: optimization basics, transformer inference and fine-tuning, generative approaches to classification, clustering/topic modeling, and parameter-efficient LLM fine-tuning.

## Contents (TPs)

- **TP2 — Mathematical optimization (foundations)**
  - Notebook: `TP2/Introduction to maths optimisation.ipynb`
  - Topics: critical points, gradients/Hessians, 1D slices, contour plots.

- **TP3 — Transformers for text classification**
  - Notebooks:
    - `TP3/Hello World Transformers.ipynb` (Hugging Face pipelines, quick start)
    - `TP3/Training Transformer Models for Text Classification.ipynb` (end-to-end fine-tuning)
  - Topics: tokenization, feature extraction, fine-tuning (DistilBERT), evaluation/error analysis, embedding visualization (UMAP).

- **TP4 — Text classification with generative models**
  - Notebook: `TP4/text_classification_generative_models.ipynb`
  - Dataset: `rotten_tomatoes`
  - Topics: task-specific classifiers, embedding-based supervised & zero-shot classification, prompted/generative classification (incl. FLAN-T5; optional API demo).

- **TP5 — Clustering and topic modeling**
  - Notebook: `TP5/clustering_and_topic_modeling.ipynb`
  - Dataset: `maartengr/arxiv_nlp`
  - Topics: sentence embeddings, UMAP, HDBSCAN clustering, BERTopic, topic/document visualization, optional LLM-assisted topic labeling.

- **TP6 — PEFT/LoRA fine-tuning of an LLM (medical)**
  - Notebook: `TP6/finetune_llama_medical.ipynb`
  - Topics: LoRA adapters with PEFT, SFT-style formatting/tokenization, training with `Trainer`, evaluation, saving adapters.
  - Artifacts:
    - `TP6/llama3_medical_lora/`: saved LoRA adapter
    - `TP6/results/`: training checkpoints
    - `TP6/evaluation_results.json`: evaluation outputs

## Quickstart

### Recommended setup (per-TP environment)

Dependencies differ between TPs (some are lightweight, others are pinned/heavier). The most reliable approach is to create **one virtual environment per TP**.

Example for TP4 (repeat for any `TPx/`):

```bash
cd TP4
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

Then open the notebook in your browser and run cells sequentially.

### Alternative (single shared environment)

If you prefer one environment for everything, be aware you may hit version conflicts between notebooks.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r TP2/requirements.txt -r TP4/requirements.txt -r TP5/requirements.txt -r TP6/requirements.txt
jupyter notebook
```

Note: `TP3/requirements.txt` is a large, fully pinned environment; using it can work as a “kitchen sink”, but it may be heavier than needed for other TPs.

## Notes

- **Hardware acceleration**
  - Many notebooks will use GPU if available (CUDA), otherwise Apple Silicon **MPS**, otherwise CPU.
- **Hugging Face authentication (TP6)**
  - Some models are gated; you may need to authenticate:
    - `huggingface-cli login`, or set `HF_TOKEN` in your environment.
- **`bitsandbytes` (TP6)**
  - `bitsandbytes` is useful for quantization on supported setups, but can be problematic on some platforms (notably macOS). If installation fails, you can usually proceed without it (CPU/MPS), or remove it from the environment for local runs.

## License

Each TP folder includes its own `LICENSE` file. See the corresponding TP directory for details.