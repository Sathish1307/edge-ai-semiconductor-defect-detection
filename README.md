# Edge-AI Semiconductor Defect Detection

## Overview
This project presents an Edge-AI based defect classification system for semiconductor wafer and die inspection images. The goal is to automatically detect and classify common manufacturing defects using lightweight AI models that are suitable for edge deployment.

The work is being developed as part of the **DeepTech Hackathon 2026 – AI-Enabled Chip Design**.

---

## Problem Statement
Modern semiconductor fabrication generates a very large number of wafer and die inspection images using optical microscopes, SEM, and similar tools. Manual and centralized inspection of these images results in high latency, bandwidth bottlenecks, and scalability challenges.

This project aims to address these challenges by building an AI-based defect classification system that can operate efficiently under edge-compute constraints.

---
## Defect Classes
The system classifies wafer inspection images into the following categories, aligned with the dataset structure and model output labels used in Phase-1:

1. center
2. clean
3. donut
4. edge_loc
5. edge_ring
6. loc
7. near_full 
8. scratch  
9. other

These classes represent commonly observed wafer-level defect patterns and spatial defect distributions used in semiconductor manufacturing inspection.

---

## Dataset Description
The dataset is created using publicly available semiconductor inspection images collected from research publications, online resources, and open datasets.

### Dataset Characteristics
- Image type: Grayscale (single-channel)
- Image source: SEM / microscope inspection images
- Total images: ≥ 500 (balanced across classes)
- Split: Train / Validation / Test

- Total images: 8,960
- Split:
  - Train: 6,515 (70%)
  - Validation: 1,219 (15%)
  - Test: 1,226 (15%)

Images are organized into class-wise folders to support supervised learning.

---

## Methodology (High-Level)
1. Image preprocessing (grayscale conversion, resizing)
2. Training a lightweight CNN-based image classification model
3. Evaluating performance using standard classification metrics
4. Exporting the trained model to ONNX format for edge portability

The emphasis is on achieving a balance between accuracy and model size.

The trained Phase-1 model is exported in ONNX format to support portability and edge deployment workflows.


---

## Evaluation Metrics
The following metrics are used to evaluate the model:
- Accuracy
- Precision
- Recall
- Confusion Matrix
- Model size (MB)

---

## Edge Deployment Readiness
The trained model is designed to be portable to edge environments. In later phases, the model is converted and prepared for deployment using the NXP eIQ workflow targeting NXP i.MX RT series devices.

---

## Dataset Access

Due to size constraints, the full dataset is not hosted directly in this GitHub repository.

The complete dataset (train/validation/test splits with class-wise organization) is available as a ZIP file at the following link:

 Dataset ZIP: https://drive.google.com/file/d/1rL4r2RSXXkeC-MuFgQvt5gifkmJeN1pZ/view?usp=sharing 

The dataset structure exactly matches the folder layout used in this repository and the class order used by the trained ONNX model.


---
## Repository Structure

The repository is organized to clearly separate data, models, source code, and documentation, following best practices for machine learning projects.

edge-ai-semiconductor-defect-detection/
├── dataset/
│   ├── train/
│   ├── val/
│   └── test/
│
├── docs/
│   ├── dataset_description.md
│   ├── dataset_source.md
│   ├── labeling_guidelines.md
│   └── README.md
│
├── models/
│   ├── wafer_final_best.onnx
│   └── README.md
│
├── results/
│   └── README.md
│
├── src/
│   ├── preprocessing/
│   ├── training/
│   ├── inference/
│   └── README.md
│
├── notebooks/
│
└── README.md

This structure ensures clear traceability between the dataset, trained ONNX model, evaluation results, and documentation used for Phase-1 submission.


