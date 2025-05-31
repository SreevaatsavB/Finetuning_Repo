# TrOCR Fine-tuning for Image Transcription

This directory contains a notebook for fine-tuning TrOCR (Transformer-based Optical Character Recognition) models for converting text in images to machine-readable text.

## Notebook Overview

### [finetune_TrOCR.ipynb](finetune_TrOCR.ipynb)

This notebook demonstrates how to fine-tune Microsoft's TrOCR model on custom image-text pairs for accurate text transcription from images.

#### Key Features:
- Loads and preprocesses custom image-text datasets
- Configures a TrOCR model for fine-tuning
- Implements training with early stopping and evaluation
- Tests and visualizes model performance on new images
- Provides utilities for model evaluation using CER (Character Error Rate)

#### Model Used:
- TrOCR: A transformer model with visual encoder and text decoder architecture
- Base model: Microsoft's TrOCR with pretrained weights

#### Fine-tuning Approach:
1. Prepares image-text pairs from a custom dataset
2. Sets up a training pipeline using Hugging Face's Transformers
3. Trains the model with optimized hyperparameters
4. Evaluates performance using Character Error Rate (CER)
5. Saves and demonstrates the fine-tuned model

#### Dataset Structure:
The notebook expects a dataset with:
- Image files (text regions)
- Corresponding ground truth text for each image

#### Evaluation:
- Character Error Rate (CER) - Lower is better
- Visual comparison of transcription results

## Requirements

- Python 3.x
- PyTorch
- Transformers
- PIL/Pillow
- Matplotlib
- Evaluate
- Jiwer (for CER calculation)
- Azure AI Form Recognizer (optional, for comparison)

## Usage

1. Prepare your dataset with image-text pairs
2. Update paths and parameters in the notebook
3. Run the cells sequentially
4. Fine-tuning parameters can be adjusted based on your needs
5. The fine-tuned model can be saved and used for OCR tasks

## Applications

The fine-tuned TrOCR model can be used for:
- Document digitization
- Receipt OCR
- License plate reading
- Text extraction from natural scene images
- Accessibility tools for converting image text to readable/spoken text
