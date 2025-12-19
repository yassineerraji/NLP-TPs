# Text Classification with Generative Models

This practical work explores **text classification with generative models**, and compares them against more traditional approaches such as **task-specific classifiers** and **embedding-based methods**.

## Overview

The notebook investigates whether generative models are effective for classification and how to measure success with standard evaluation metrics.
It uses the `rotten_tomatoes` dataset (movie reviews labeled **positive** or **negative**).

## Key Topics

- **Task-specific classification** with a pretrained sentiment model (RoBERTa-based)
- **Supervised classification with embeddings**: generate embeddings and train a lightweight classifier (e.g., logistic regression)
- **Zero-shot classification with embeddings**: classify by comparing document embeddings to label-description embeddings (cosine similarity)
- **Generative classification** with prompts (LLM API demo) and **text-to-text** models (T5/FLAN-T5)
- **Evaluation** using `classification_report` (precision / recall / F1 / accuracy)

## Technologies Used

- **Transformers (Hugging Face)**: pipelines + pretrained models (RoBERTa, FLAN-T5)
- **PyTorch**: Deep learning framework
- **Datasets (Hugging Face)**: Dataset loading and management
- **NumPy**: Numerical operations
- **tqdm**: Progress bars for long-running operations
- **scikit-learn**: evaluation + simple classifiers
- **sentence-transformers**: sentence embeddings
- **groq** (optional): API-based LLM demo

## Contents

The notebook follows this progression:
1. Load the Rotten Tomatoes dataset
2. Run a task-specific sentiment classifier and evaluate it
3. Train a classifier on top of frozen embeddings (supervised)
4. Perform zero-shot classification with embeddings
5. Try generative approaches (prompted LLM + text-to-text with FLAN-T5)

## Installation

1. Install the required dependencies:

```bash
pip install -r requirements.txt
```

2. Launch Jupyter Notebook:

```bash
jupyter notebook
```

3. Open `text_classification_generative_models.ipynb`

## Usage

Run the cells sequentially. Each section is self-contained and ends with an evaluation so you can compare approaches directly.

## Dataset

The Rotten Tomatoes dataset contains movie reviews with binary sentiment labels, making it a simple benchmark for comparing classification strategies.

