# Models

This folder contains trained machine learning models for the semiconductor defect classification system.

## Phase-1 Model
- Format: ONNX
- File: wafer_final_best.onnx
- Task: Multi-class wafer defect classification
- Classes:
  - center
  - clean
  - donut
  - edge_loc
  - edge_ring
  - loc
  - near_full
  - other
  - scratch

The model is trained using grayscale wafer inspection images and is optimized for edge deployment in later phases.

