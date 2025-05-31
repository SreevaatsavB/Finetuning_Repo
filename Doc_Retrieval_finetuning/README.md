# Document Retrieval Fine-tuning

This directory contains notebooks for fine-tuning sentence transformer models for document retrieval tasks.

## Notebook Overview

### [finetune_retrieval_sentance_transformers.ipynb](finetune_retrieval_sentance_transformers.ipynb)

This notebook demonstrates how to fine-tune a Sentence Transformer model for improved document retrieval performance using the Natural Questions dataset.

#### Key Features:
- Loads and preprocesses the Natural Questions dataset
- Sets up a fine-tuning pipeline for sentence transformers
- Implements contrastive learning with hard negatives
- Evaluates model performance using NDCG metrics
- Compares baseline vs. fine-tuned model performance
- Visualizes performance improvements

#### Model Used:
- Base Model: `sentence-transformers/all-MiniLM-L6-v2`

#### Dataset:
- Natural Questions dataset from HuggingFace (`sentence-transformers/natural-questions`)

#### Fine-tuning Approach:
1. Prepares triplets of (query, positive document, negative document)
2. Uses Multiple Negative Ranking Loss for training
3. Runs for multiple epochs with learning rate scheduling
4. Evaluates on validation and test sets

#### Evaluation Metrics:
- NDCG (Normalized Discounted Cumulative Gain)
- The notebook visualizes improvements in retrieval quality

## Requirements

- Python 3.x
- PyTorch
- sentence-transformers
- datasets
- huggingface_hub
- matplotlib
- pandas

## Usage

1. Open the notebook in a Jupyter environment
2. Run the cells sequentially
3. Fine-tuning parameters can be adjusted in the notebook
4. The fine-tuned model can be saved and used for document retrieval tasks

## Results

The notebook demonstrates significant improvements in retrieval quality after fine-tuning, visualized through comparison charts between the base model and fine-tuned model.
