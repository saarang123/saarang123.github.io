---
layout: page
title: TPGNN - Learned Cost Model for Tensor Program Optimization
description: Tensor Program Optimization using Graph Neural Networks
img: assets/img/tvm.png
importance: 1
category: work
related_publications: false
---

## Project Overview
TPGNN introduces a novel approach to optimizing machine learning compiler performance using Graph Neural Networks (GNNs). Traditional ML compilers like TVM use simple cost models like XGBoost to predict program runtime and guide optimizations. However, these models often fail to capture complex program dependencies. Our work replaces TVM's default cost model with a sophisticated GNN that learns from the program's Abstract Syntax Tree (AST), enabling more accurate runtime predictions and better optimization decisions.

## Technical Implementation

### Feature Engineering and Data Processing
- Developed custom embeddings for 55 distinct node types in TVM's Tensor IR using FastText
- Created node feature vectors combining type embeddings and constant values
- Processed dataset of 131 workloads from TenSet, containing ~60K samples with varying graph sizes
- Implemented advanced data preprocessing including Z-score normalization for numerical stability

### GNN Architecture
- Built a hierarchical GNN with 3 message-passing layers using graph convolutions
- Incorporated TopK pooling layers to handle large ASTs efficiently
- Designed a multi-layer architecture combining:
  - Graph convolutional layers for local feature extraction
  - Hierarchical pooling for graph structure learning
  - Global pooling for final graph representation
  - MLP layers for runtime prediction

### Integration with TVM
- Modified TVM's AutoScheduler to support GNN-based cost predictions
- Implemented custom data extraction pipeline for converting TensorIR to graph format
- Developed efficient feature computation and model inference pathways

## Results and Impact
Our model achieved:
- 33% improvement in prediction accuracy compared to XGBoost on test workloads
- Successful validation on real ML architectures including ResNet-18, MobileNet, and Inception v3
- Better generalization to unseen workload types due to structural understanding

{% include figure.liquid loading="eager" path="assets/img/workflow.png" title="TPGNN Workflow" class="img-fluid rounded z-depth-1" %}
*High-level architecture of TPGNN showing the workflow from TensorIR to runtime prediction*

## Tools and Technologies
- PyTorch & PyTorch Geometric for GNN implementation
- TVM for compiler infrastructure
- FastText for node embedding generation
- Python multiprocessing for parallel data processing
- CUDA for GPU acceleration

## Code and Resources
- [TPGNN Implementation](https://github.com/knightron0/tvm-gnn-costmodel)
- [Modified TVM Fork](https://github.com/dwijenchawra/tvm)