---
layout: page
title: TPGNN - Learned Cost Model for Tensor Program Optimization
description: Tensor Program Optimization using Graph Neural Networks
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---


Tensor program optimization is essential for boosting the efficiency of machine learning systems, particularly in edge applications requiring low latency and high throughput. Traditional methods depend on hardware-specific rules or search-based strategies combined with learned cost models for performance tuning. In this project, we present a novel learned cost model for tensor programs leveraging Graph Neural Networks (GNNs). We capture global semantics and dependencies by embedding the abstract syntax tree (AST) of tensor programs into a GNN, enabling precise execution cost predictions. Our approach focuses on runtime prediction specifically for NVIDIA V100 GPUs, delivering accurate and hardware-specific optimization to improve performance in machine learning workloads.


To evaluate the effectiveness of our model, we integrate it into TVM’s AutoScheduler framework. TVM is an open-source machine learning compiler stack that automates tensor program optimization. We replace TVM’s default cost model (XGBoost) with our GNN-based model and use TVM’s AutoScheduler to fine-tune and optimize tensor programs. We further evaluate our model on datasets such as TenSet where our model's outperforms XGBoost in terms of accuracy. 

Code Repository: [https://github.com/knightron0/tvm-gnn-costmodel](https://github.com/knightron0/tvm-gnn-costmodel)
TVM Fork: [https://github.com/dwijenchawra/tvm](https://github.com/dwijenchawra/tvm)



