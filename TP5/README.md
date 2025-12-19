# Clustering and Topic Modeling

This practical work explores **text clustering** and **topic modeling** on research paper abstracts from ArXiv, using modern embedding models and BERTopic.

## Overview

The notebook demonstrates a full workflow for organizing a large collection of documents:
- group similar documents together (clustering)
- extract human-interpretable themes for each group (topic modeling)

This is useful for understanding research landscapes, identifying trends, and navigating large corpora.
The dataset used is `maartengr/arxiv_nlp` (titles + abstracts from ArXiv NLP papers).

## Key Topics

- **Semantic embeddings** for representing documents
- **Dimensionality reduction** with UMAP (both for clustering and 2D visualization)
- **Density-based clustering** with HDBSCAN
- **Topic modeling** with BERTopic (c-TF-IDF topic representations)
- **Visualization** of documents/topics (Matplotlib + interactive BERTopic visualizations / DataMapPlot)
- **(Optional)** LLM-assisted topic labeling (text generation)

## Technologies Used

- **Sentence Transformers**: generating semantic embeddings optimized for similarity tasks
- **BERTopic**: topic modeling pipeline on top of embeddings + clustering
- **UMAP**: Dimensionality reduction for visualization
- **HDBSCAN**: density-based clustering (automatic number of clusters + outlier handling)
- **Datasets (Hugging Face)**: Loading the ArXiv dataset
- **DataMapPlot**: Interactive visualization of embeddings

## Contents

The notebook follows a standard pipeline:

1. **Embedding**: Transform documents into numerical embeddings using sentence transformers
2. **Dimensionality Reduction**: Compress embeddings using UMAP
3. **Clustering**: Identify semantically related document clusters
4. **Topic Modeling**: Extract topics from clusters using BERTopic
5. **Visualization**: Create interactive visualizations of the results

## Installation

1. Install the required dependencies:

```bash
pip install -r requirements.txt
```

2. Launch Jupyter Notebook:

```bash
jupyter notebook
```

3. Open `clustering_and_topic_modeling.ipynb`

## Usage

Run the cells sequentially. Each major stage (embedding → clustering → topic modeling) produces artifacts you can inspect (clusters, keywords, plots).

## Dataset

The ArXiv NLP dataset contains abstracts and titles from research papers, making it a strong use case for clustering and topic modeling to understand research trends and identify related work.

## Notes

- Choose embedding models optimized for semantic similarity (check the [embedding benchmark](https://huggingface.co/spaces/mteb/leaderboard))
- Dimensionality reduction involves a trade-off between compression and information retention
- The notebook uses `thenlper/gte-small` as a lightweight embedding model suitable for various hardware configurations

