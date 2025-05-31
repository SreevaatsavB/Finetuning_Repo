# OCR Fine-tuning

This directory contains notebooks for fine-tuning models related to Optical Character Recognition (OCR) tasks, divided into two main components:

1. **Image Transcription** - Converting text in images to machine-readable text
2. **Text Detection** - Detecting and localizing text regions in images

## Directory Structure

```
OCR_finetuning/
├── Image_trascription/
│   └── finetune_TrOCR.ipynb      # Fine-tuning TrOCR for image text transcription
└── Text_detection/
    ├── finetune_text_detection.ipynb  # Fine-tuning YOLO for text region detection
    └── prepare_data.ipynb        # Preparing data for text detection training
```

## Module Overview

### Image Transcription

The Image Transcription module focuses on fine-tuning transformer-based OCR models (TrOCR) that can accurately convert text in images to machine-readable text. This is particularly useful for digitizing documents, extracting text from images, and creating accessible versions of image-based content.

### Text Detection

The Text Detection module contains notebooks for fine-tuning YOLO models to detect and localize text regions in images. This is an essential preprocessing step for many OCR pipelines, especially when dealing with complex documents or images where text is mixed with other visual elements.

## Getting Started

Each subdirectory contains detailed notebooks with step-by-step instructions. Navigate to the specific task you're interested in:

- For image-to-text transcription: [Image_trascription/finetune_TrOCR.ipynb](Image_trascription/finetune_TrOCR.ipynb)
- For text region detection: [Text_detection/finetune_text_detection.ipynb](Text_detection/finetune_text_detection.ipynb)
- For preparing text detection data: [Text_detection/prepare_data.ipynb](Text_detection/prepare_data.ipynb)

## Requirements

The notebooks in this directory require:
- Python 3.x
- PyTorch
- Transformers (for TrOCR)
- Ultralytics (for YOLO)
- PIL/Pillow
- OpenCV
- Matplotlib
- Specific OCR-related libraries mentioned in the notebooks
