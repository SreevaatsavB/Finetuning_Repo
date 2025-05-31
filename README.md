# AI Model Fine-tuning Repository

This repository contains a collection of Jupyter notebooks and examples for fine-tuning various AI models for different tasks. Each directory focuses on a specific model type or application area.

## Repository Structure

```
Finetuning_Repo/
├── Doc_Retrieval_finetuning/      # Fine-tuning sentence transformers for document retrieval
├── LLM_finetuning/                # Fine-tuning Language Models
├── OCR_finetuning/                # OCR model fine-tuning
│   ├── Image_trascription/        # Fine-tuning for image-to-text transcription (TrOCR)
│   └── Text_detection/            # Fine-tuning for text detection in images (YOLO)
├── RAG_Reranker_finetuning/       # Fine-tuning rerankers for RAG systems
└── VLM_finetuning/                # Fine-tuning Vision Language Models
```

## Modules Overview

### Doc_Retrieval_finetuning
Contains notebooks for fine-tuning sentence transformer models for document retrieval tasks. Improves embedding quality for specific domains.

### LLM_finetuning
Resources for fine-tuning Large Language Models for various text generation tasks.

### OCR_finetuning
Contains two sub-modules:
- **Image_trascription**: Fine-tune TrOCR models for converting image text to typed text
- **Text_detection**: Fine-tune YOLO models for detecting text regions in images

### RAG_Reranker_finetuning
Notebooks for fine-tuning reranker models used in Retrieval-Augmented Generation (RAG) pipelines.

### VLM_finetuning
Resources for fine-tuning Vision-Language Models for multimodal tasks.

## Getting Started

Each directory contains specific notebooks with detailed instructions. Navigate to the directory of interest and refer to its README and Jupyter notebooks for task-specific guidance.

## Requirements

Each notebook specifies its own requirements, but common dependencies include:
- Python 3.x
- PyTorch
- Transformers
- Datasets
- Specific model libraries (like sentence-transformers, YOLO, etc.)

For detailed requirements, see the specific notebook you wish to run.
