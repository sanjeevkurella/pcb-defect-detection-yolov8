# pcb-defect-detection-yolov8
AI-based PCB defect detection using YOLOv8 with real-time inference
# AI-Based PCB Defect Detection using YOLOv8

## Overview

This project presents an AI-based system for detecting defects in Printed Circuit Boards (PCBs) using the YOLOv8 object detection algorithm. The system identifies and classifies multiple defect types and provides real-time predictions with severity-based decision logic.

## Features

* Detection of 6 PCB defect classes:

  * Short Circuit
  * Open Circuit
  * Missing Hole
  * Spur
  * Mouse Bite
  * Spurious Copper
* Real-time object detection using YOLOv8
* Confidence-based filtering and Non-Maximum Suppression (NMS)
* Severity classification (Critical / Moderate / Low)
* Final ACCEPT / REJECT decision logic
* Web interface built using Streamlit

## Tech Stack

* Python
* YOLOv8 (Ultralytics)
* OpenCV
* PyTorch
* Streamlit

## Dataset

* 3079 PCB images collected from Roboflow Universe
* Images resized to 640×640
* Data augmentation:

  * Brightness adjustment
  * Exposure variation
  * Rotation
  * Horizontal flipping

## Model Training

* Model: YOLOv8n
* Training platform: Google Colab (T4 GPU)
* Epochs: 25
* Batch size: 16

## Results

* mAP50: 98.4%
* Precision: 96.1%
* Recall: 96.2%
* Inference time: ~70 ms per image

## Working

1. Input PCB image
2. Image preprocessing (resize, normalization)
3. Feature extraction using YOLOv8 backbone
4. Object detection and classification
5. Post-processing (NMS + confidence filtering)
6. Severity classification
7. Final ACCEPT / REJECT decision

## Demo

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/ab4b8cfe-6579-47de-946e-6478f6a21dc5" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/e569bbf4-3c4c-4c86-a208-f11f563b751c" />

## Future Improvements

* Improve localization accuracy (mAP50-95)
* Extend to component-level defect detection
* Deploy on edge devices

## Author

Sanjeev Kurella
