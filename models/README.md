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

### Model Input Specification

- Input type: Grayscale wafer map
- Input shape: 52 × 52 pixels
- Channels: Single-channel (1)

## ONNX Output Class Order

The ONNX model outputs a probability vector across 9 classes.
The class index mapping is as follows:

0. center  
1. clean  
2. donut  
3. edge_loc  
4. edge_ring  
5. loc  
6. near_full  
7. other  
8. scratch
