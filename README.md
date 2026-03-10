
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

```
Drone-Object-Detection
│
├── Faster-RCNN/        # Faster RCNN implementation
├── MaskRCNN/           # Mask RCNN implementation
├── rcnn/               # RCNN implementation
├── SSD/                # SSD detector implementation
│
├── Yolo-v3/            # YOLOv3 training notebooks
├── yolov5/             # YOLOv5 implementation
├── Yolo-V8/            # YOLOv8 implementation
│
├── Yolo-V3-Demo/       # YOLOv3 demo inference
├── Yolo-V5-Demo/       # YOLOv5 demo inference
│
├── images/             # Example detection outputs
│
├── RCNN.ipynb          # Notebook implementation
├── content.zip         # Dataset / assets
└── README.md
```

---

# ⚙️ Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Srinivas-jatothu/Drone-Object-Detection.git
cd Drone-Object-Detection
```

### 2️⃣ Create a virtual environment (recommended)

```bash
python -m venv venv
venv\Scripts\activate
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```


---
# ▶️ Running the Models

Most implementations are provided as **Jupyter notebooks**.

You can run them using:

- **Google Colab**
- **Kaggle**
- **Local GPU machine**

Typical workflow:

1. Download VisDrone dataset
2. Configure dataset paths
3. Run training notebook
4. Evaluate detection performance
5. Visualize predictions
---
# 📊 Evaluation Metrics

The models are evaluated using standard object detection metrics:

- **mAP (Mean Average Precision)**
- **Precision**
- **Recall**
- **PR Curve**
- **Inference Time**

These metrics help analyze both **accuracy** and **real-time performance**.

---

# 🚀 Applications

Potential real-world applications of aerial object detection include:

- Autonomous drone monitoring
- Smart traffic management
- Disaster assessment
- Border surveillance
- Wildlife monitoring

---

# 🔮 Future Improvements

Possible extensions for this project include:

- Training on **larger UAV datasets**
- Using **Vision Transformers for detection**
- Deploying models on **edge devices**
- Integrating **multi-object tracking**
- Improving small-object detection

---

# 📚 References

- YOLOv5 — Ultralytics
- YOLOv8 — Ultralytics
- Faster RCNN — Ren et al.
- Mask RCNN — He et al.
- VisDrone Dataset

Dataset Source:
https://paperswithcode.com/dataset/visdrone

---

# 👨‍💻 Author

**Srinivas Jatothu**

GitHub:
https://github.com/Srinivas-jatothu
