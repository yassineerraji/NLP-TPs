# Fine-tuning Llama 3.2 on Medical Dataset

This practical work demonstrates how to fine-tune a large language model (LLM) with **Parameter-Efficient Fine-Tuning (PEFT)**, using **LoRA (Low-Rank Adaptation)** on a medical question-answer dataset.

## Overview

The notebook (`finetune_llama_medical.ipynb`) walks through an end-to-end workflow:
- load a causal LM (TinyLlama by default, Llama 3.2 if you have access)
- attach a LoRA adapter with PEFT
- format + tokenize a medical dataset for supervised fine-tuning
- train with the Hugging Face `Trainer`
- evaluate and save artifacts for later inference

## Key Topics

- **LoRA fine-tuning** for causal language models
- **PEFT adapters**: train a small number of parameters instead of full fine-tuning
- **Prompt formatting** for chat/instruct-style models
- **Training + saving** LoRA adapter weights
- **Evaluation** (simple exact/partial match heuristics) and inference

## Technologies Used

- **Transformers (Hugging Face)**: Model loading and training utilities
- **PyTorch**: Deep learning framework
- **PEFT**: Parameter-Efficient Fine-Tuning library for LoRA
- **Datasets (Hugging Face)**: Medical dataset loading
- **Hugging Face Hub**: Model and dataset management

## Contents

The notebook follows a complete training pipeline:

1. **Model Loading**: Load Llama 3.2 or TinyLlama model and tokenizer
2. **PEFT Configuration**: Set up LoRA configuration for efficient fine-tuning
3. **Data Preparation**: Load and preprocess medical dataset
4. **Training**: Fine-tune the model using the Trainer API
5. **Evaluation**: Assess model performance on test data
6. **Inference**: Test the fine-tuned model with sample queries
7. **Saving**: Save the adapter weights for later use

## Installation

1. Install the required dependencies:

```bash
pip install -r requirements.txt
```

2. Authenticate with Hugging Face (required for gated models like Llama):

Option A (recommended): log in once via CLI:

```bash
huggingface-cli login
```

Option B: set an environment variable (useful in notebooks/CI):

```bash
export HF_TOKEN="your_token_here"
```

3. Launch Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `finetune_llama_medical.ipynb`

## Usage

Run the cells sequentially. The notebook automatically selects the best available device:
- **CUDA** (NVIDIA GPU) if available
- **MPS** (Apple Silicon) if available
- otherwise **CPU**

By default, it uses **TinyLlama** to avoid gated access. You can switch to **Llama 3.2** once your account is approved.

## Model Files

This directory contains:
- `llama3_medical_lora/`: Fine-tuned LoRA adapter weights
- `results/checkpoint-50/`: Training checkpoint with optimizer states
- `evaluation_results.json`: Model evaluation metrics

## Notes

- LoRA allows fine-tuning with significantly fewer parameters than full fine-tuning
- The notebook uses FP16 precision for memory efficiency
- For production use, ensure you have proper access to Llama models from Meta
- Medical datasets require careful handling and may have specific licensing requirements

