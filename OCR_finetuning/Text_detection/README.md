# Text Detection Fine-tuning

This directory contains notebooks for fine-tuning YOLO models to detect and localize text regions in images.

## Notebook Overview

### [finetune_text_detection.ipynb](finetune_text_detection.ipynb)

This notebook demonstrates how to fine-tune YOLOv8 for text detection in images.

#### Key Features:
- Loads a pre-trained YOLOv8 model and adapts it for text detection
- Configures training parameters for optimal text detection
- Fine-tunes the model on text detection datasets
- Evaluates and visualizes detection performance
- Provides utilities for testing on new images

#### Model Used:
- YOLOv8 (options include yolov8n.pt, yolov8s.pt, yolov8m.pt, yolov8l.pt, yolov8x.pt)
- The notebook uses YOLOv8L by default for a good balance of speed and accuracy

#### Fine-tuning Approach:
1. Loads a pre-trained YOLO model from Ultralytics
2. Configures the model for single-class detection (text)
3. Sets training parameters (image size, batch size, learning rate, etc.)
4. Trains the model on prepared text detection datasets
5. Evaluates performance using precision, recall, and mAP metrics

#### Evaluation:
- Precision, Recall, mAP50, mAP50-95
- Visualization of detection results on test images

### [prepare_data.ipynb](prepare_data.ipynb)

This notebook guides you through preparing and formatting data for text detection training.

#### Key Features:
- Converts various text detection datasets to YOLO format
- Performs data cleaning and normalization
- Creates train/validation splits
- Generates a dataset.yaml configuration file

#### Data Preparation Steps:
1. Loads and processes source datasets
2. Converts bounding box formats to YOLO format
3. Creates directory structure required by YOLOv8
4. Generates a dataset.yaml file for training

## Requirements

- Python 3.x
- PyTorch
- Ultralytics YOLOv8
- OpenCV
- Matplotlib
- Pandas
- PIL/Pillow

## Usage

1. First run [prepare_data.ipynb](prepare_data.ipynb) to set up your dataset
2. Then run [finetune_text_detection.ipynb](finetune_text_detection.ipynb) to fine-tune the model
3. Parameters can be adjusted based on your hardware and dataset
4. The fine-tuned model can be exported to various formats (ONNX, TensorRT, etc.)

## Applications

The fine-tuned text detection model can be used for:
- Locating text in natural scene images
- Pre-processing documents for OCR pipelines
- Identifying text regions in mixed-content documents
- Real-time text detection in videos or camera feeds
