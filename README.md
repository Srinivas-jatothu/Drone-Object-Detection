
# 🚁 DroneVision: Deep Learning for Aerial Object Detection

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

DroneVision is a deep learning project that focuses on detecting objects from aerial images captured by drones. The repository evaluates multiple object detection models and compares their performance using the **VisDrone2019 dataset**, which is designed for UAV-based surveillance applications.

This project investigates how different deep learning architectures perform when detecting small, dense, and occluded objects from aerial viewpoints.

---

# 📌 Project Overview

Drone-based vision systems are increasingly used in areas such as:

- Traffic monitoring
- Smart city surveillance
- Disaster response
- Crowd monitoring
- Security systems

However, detecting objects in drone footage is challenging due to:

- Objects appearing **very small**
- **Large variations in scale**
- **Complex backgrounds**
- **High object density**
- **Perspective distortion from aerial view**

To study these challenges, this project benchmarks several object detection models ranging from traditional **Two-Stage detectors** to modern **Real-Time One-Stage detectors**.

---

# 🧠 Models Implemented

The repository contains implementations of several object detection architectures.

## Two-Stage Object Detectors

These models first generate candidate regions and then classify objects inside them.

- **RCNN**
- **Faster RCNN**
- **Mask RCNN**

Two-stage detectors generally achieve higher localization accuracy but are computationally heavier.

---

## One-Stage Object Detectors

These models detect objects directly in a single pass through the network.

- **SSD (Single Shot Detector)**
- **YOLOv3**
- **YOLOv5**
- **YOLOv8**

One-stage detectors are optimized for **real-time detection**, making them suitable for drone and edge deployments.

---

# 📊 Experimental Results

The models were trained and evaluated on the **VisDrone-DET benchmark dataset**.

| Model                  | mAP@0.5        | Inference Time (ms) | Category  |
| ---------------------- | -------------- | ------------------- | --------- |
| **YOLOv8 Large** | **0.56** | **3.53**      | One-Stage |
| YOLOv5 Large           | 0.54           | 12.10               | One-Stage |
| YOLOv3                 | 0.40           | 22.00               | One-Stage |
| RCNN                   | 0.30           | 190.00              | Two-Stage |
| Mask RCNN              | 0.29           | 200.00              | Two-Stage |
| Faster RCNN            | 0.23           | 150.00              | Two-Stage |
| SSD                    | 0.12           | 30.00               | One-Stage |

**Key Observation**

YOLOv8 achieved the best balance between detection accuracy and inference speed, making it highly suitable for real-time aerial monitoring.

---

# 📂 Repository Structure
