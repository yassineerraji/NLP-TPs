# Transformer Models for Text Classification

This practical work explores the Hugging Face Transformers library and demonstrates how to use pre-trained transformer models for text classification tasks.

## Overview

This directory contains two notebooks:

### 1. Hello World Transformers
An introduction to the Hugging Face library using pre-trained models for text classification. This notebook covers:
- Understanding Hugging Face pipelines
- Using pre-trained models for sentiment analysis
- Basic text classification with transformers

### 2. Training Transformer Models for Text Classification
A comprehensive guide to training transformer models for emotion classification from Twitter messages. This notebook covers:
- Loading and exploring datasets from Hugging Face Hub
- Understanding tokenization strategies (character, word, subword)
- Using transformers as feature extractors
- Fine-tuning transformer models (DistilBERT) for classification
- Model evaluation and error analysis
- Visualizing embeddings with UMAP
- Saving and sharing models on Hugging Face Hub

## Technologies Used

- **Transformers (Hugging Face)**: Pre-trained transformer models and utilities
- **PyTorch**: Deep learning framework
- **Datasets (Hugging Face)**: Dataset loading and preprocessing
- **scikit-learn**: Machine learning utilities and metrics
- **UMAP**: Dimensionality reduction for visualization
- **Matplotlib/Seaborn**: Data visualization

## Structure

- `Hello World Transformers.ipynb`: Introduction to Hugging Face pipelines
- `Training Transformer Models for Text Classification.ipynb`: Complete training pipeline from data loading to model deployment

## Installation

1. Install the required dependencies:
```bash
pip install -r requirements.txt
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```

3. Open the notebook you want to explore

## Usage

Start with "Hello World Transformers" to get familiar with the basics, then proceed to "Training Transformer Models" for a complete end-to-end training experience.

## Dataset

The training notebook uses the emotion recognition dataset from Hugging Face, which contains Twitter messages labeled with six emotions: anger, disgust, fear, joy, sadness, and surprise.

