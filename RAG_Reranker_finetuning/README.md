# RAG Reranker Fine-tuning

This directory contains notebooks for fine-tuning reranker models used in Retrieval-Augmented Generation (RAG) pipelines. Rerankers help improve the quality of retrieved documents by reordering them based on their relevance to a query.

## Directory Structure

```
RAG_Reranker_finetuning/
├── Eval_bge_reranker.ipynb          # Evaluation of BGE reranker model
├── finetune_reranker.ipynb          # Fine-tuning reranker models
├── lora_Eval_bge_reranker.ipynb     # Evaluation of LoRA-based BGE reranker
├── lora_finetuning_reranker.ipynb   # Fine-tuning rerankers using LoRA
└── data/                            # Data directory for training examples
```

## Notebook Overview

### [finetune_reranker.ipynb](finetune_reranker.ipynb)

This notebook demonstrates how to fine-tune a reranker model on custom data for improving document ranking in RAG systems.

#### Key Features:
- Fine-tunes BGE (BAAI General Embedding) reranker models
- Configures training parameters for reranking tasks
- Trains cross-encoder models for accurate passage ranking
- Uses FlagEmbedding library for efficient training

#### Models Used:
- `BAAI/bge-base-en-v1.5`
- `BAAI/bge-large-en-v1.5`
- `BAAI/bge-reranker-v2-m3`

#### Fine-tuning Approach:
1. Prepares training data with queries and relevant/non-relevant passages
2. Configures a cross-encoder architecture for reranking
3. Trains with pairwise ranking loss
4. Evaluates reranking performance

### [Eval_bge_reranker.ipynb](Eval_bge_reranker.ipynb)

This notebook provides methods for evaluating the performance of BGE reranker models.

#### Key Features:
- Loads and tests reranker models
- Evaluates reranking performance on test queries
- Compares performance metrics between different models
- Visualizes ranking improvements

### [lora_finetuning_reranker.ipynb](lora_finetuning_reranker.ipynb)

This notebook shows how to fine-tune reranker models using LoRA (Low-Rank Adaptation) for more efficient training.

#### Key Features:
- Implements LoRA for parameter-efficient fine-tuning
- Requires less memory and compute compared to full fine-tuning
- Maintains high performance while reducing training resources
- Practical for larger models and limited hardware

### [lora_Eval_bge_reranker.ipynb](lora_Eval_bge_reranker.ipynb)

This notebook evaluates the performance of LoRA-fine-tuned reranker models.

#### Key Features:
- Tests LoRA-adapted rerankers
- Compares performance to full fine-tuning approach
- Verifies that parameter-efficient training maintains quality
- Provides metrics and examples of improved rankings

## Requirements

- Python 3.x
- PyTorch
- Transformers
- FlagEmbedding
- Pandas
- Matplotlib
- Accelerate (for LoRA training)
- Unsloth (optional, for optimization)

## Usage

1. Prepare your query-document pairs in the expected format
2. Choose between standard fine-tuning ([finetune_reranker.ipynb](finetune_reranker.ipynb)) or LoRA ([lora_finetuning_reranker.ipynb](lora_finetuning_reranker.ipynb))
3. Run the training notebook
4. Evaluate the model using the corresponding evaluation notebook
5. The fine-tuned model can be integrated into RAG pipelines for improved document ranking

## Applications

Reranker models are crucial for:
- Improving RAG system performance by providing more relevant context
- Enhancing search results by reordering retrieved documents
- Creating more effective information retrieval systems
- Reducing hallucinations in generative AI by prioritizing relevant information
