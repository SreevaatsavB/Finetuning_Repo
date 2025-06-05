# FLUX Image Generation

This directory contains resources for fine-tuning and using FLUX (Flow-based Linear Unified eXtensions) image generation models, which are part of the diffusers library for controlled image generation.

## Directory Structure

```
FLUX_image_generation/
├── train_conditional_generation.ipynb   # Notebook for fine-tuning FLUX models
└── Inference/                           # Inference examples for FLUX models
    ├── flux-canny-edge-inference.ipynb  # Inference using canny edge detection for control
    └── flux-shnell-inference-pipeline.ipynb  # Using SHNELL pipeline with FLUX for inference
```

## Overview

FLUX (Flow-based Linear Unified eXtensions) is an advanced technique for controllable image generation. The notebooks in this directory demonstrate how to:

1. **Fine-tune FLUX models**: Customize image generation models with control mechanisms to generate images based on specific conditions or inputs.

2. **Run inference with FLUX**: Use pre-trained FLUX models to generate images with various control mechanisms, including:
   - Canny edge detection-based control
   - SHNELL pipeline for enhanced control

## Requirements

The notebooks include installation of required dependencies. Major requirements include:

- PyTorch
- Diffusers (latest development version)
- Transformers
- Accelerate
- PEFT (Parameter-Efficient Fine-Tuning)
- XFormers (for memory optimization)

## Getting Started

1. Open the `train_conditional_generation.ipynb` notebook to learn how to fine-tune FLUX models
2. Use the notebooks in the `Inference` directory to run inference with pre-trained FLUX models

## References

- [Hugging Face Diffusers Library](https://github.com/huggingface/diffusers)
- [FLUX Documentation](https://huggingface.co/docs/diffusers/main/en/using-diffusers/flux)
