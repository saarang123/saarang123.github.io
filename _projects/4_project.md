---
layout: page
title: Real-Time Anomaly Detection for Industrial IoT
description: ML-powered anomaly detection system for industrial equipment
img: assets/img/webee.jpeg
importance: 4
category: work
---

## Overview

Developed an end-to-end IoT and machine learning solution for [Webee.io](https://www.webee.io/) to enable real-time equipment monitoring and failure prediction in industrial settings. This was part of my work with The Purdue Data Mine Learning Community.

## Technical Details

### Data Processing Pipeline

- Engineered robust data cleaning pipeline for noisy sensor data using:
  - Linear regression for trend analysis and outlier detection
  - Gaussian Mixture Models (GMM) for multi-modal noise clustering
  - Kalman filtering for sensor fusion and state estimation
- Achieved 93% accuracy in noise reduction while preserving critical signal features
- Implemented real-time data processing using Apache Kafka streams

### Machine Learning System

- Developed hybrid anomaly detection system combining:
  - One-Class SVM for novelty detection
  - LSTM networks for sequence-based pattern recognition
  - Achieved 83% accuracy in anomaly detection with low false positive rate
- Implemented online learning to adapt to concept drift in sensor patterns
- Built custom feature extraction for various sensor types (vibration, temperature, pressure)
- Completely unsupervised learning process since the data was unlabeled.

### System Architecture

- Designed IoT product architecture using Docker and Kubernetes ensuring ease of deployment and scalability.
- Built real-time alerting system with configurable thresholds and notification channels
- No evaluation was done from Webee.io side but the system aligns

## Poster/Report

For more details, you can view the full project report here:

<object data="{{ site.baseurl }}/assets/pdf/webee_report.pdf" type="application/pdf" width="100%" height="600px">
    <p>It appears you don't have a PDF plugin for this browser.
    You can <a href="{{ site.baseurl }}/assets/pdf/webee_report.pdf">click here to download the PDF file.</a></p>
</object>
