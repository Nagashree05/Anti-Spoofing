# 🛡️ Anti-Spoofing Project: Safeguarding Biometric Systems

## Overview
This project explores the application of **deep learning** to counter **face presentation attacks (FPA)** in biometric authentication systems. By leveraging **ResNet50** and **EfficientNetB7**, two state-of-the-art CNN architectures, we rigorously evaluated their performance on the challenging **SynthASpoof** dataset to determine the most reliable model for detecting spoofing attempts.

## Objective
To develop and benchmark deep learning models that can accurately distinguish between **bonafide (real)** and **spoofed (fake)** face images, including advanced attacks like **video replays**, using the SynthASpoof dataset.

## Dataset: [SynthASpoof]
A large-scale synthetic dataset containing a diverse set of face presentation attacks:
- **Bonafide (Genuine)** images
- **Printed** image attacks
- **Replay** (video) attacks
- **Webcam replay** attacks

> The dataset was split into:
- **70% Training**
- **15% Validation**
- **15% Testing**

## Models Used

### ResNet50
- Deep 50-layer CNN
- Residual connections for efficient gradient flow
- **Achieved best performance on all metrics**

### EfficientNetB7
- Efficient and scalable architecture
- Lower number of parameters
- Needed more fine-tuning for complex spoof types

## Results Summary

| Metric                     | ResNet50       | EfficientNetB7   |
|---------------------------|----------------|------------------|
| **Test Accuracy**         | 87%            | 69%              |
| **Training & Val Loss**   | Lower & stable | Higher & fluctuating |
| **Confusion Matrix**      | High TP, Low FN| Misclassified many bonafide & webcam replays |
| **Generalization**        | Strong         | Moderate         |

> **ResNet50 outperformed EfficientNetB7** in classification accuracy, robustness to attack types, and training convergence.

## Evaluation Metrics
- **Accuracy**
- **Loss curves (training/validation)**
- **Confusion Matrix**
- **Precision / Recall / F1-Score**


## Why This Matters
Face spoofing attacks (like printed photos or replay videos) pose serious threats to the integrity of biometric systems. This project provides:
- A validated model architecture for anti-spoofing
- A benchmark on the SynthASpoof dataset
- Insights into model behavior on complex spoof types
