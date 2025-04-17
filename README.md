# CAPTCHA Text Recognition 🧠🔐

This project focuses on building a deep learning model to automatically recognize text from CAPTCHA images using a **ResNet-based architecture**. The system aims to streamline CAPTCHA decoding using computer vision and deep learning techniques.

---

## ❓ Problem Statement

CAPTCHAs are used as security checkpoints to differentiate humans from bots when accessing websites. This project aims to break CAPTCHAs using a learning-based approach, leveraging deep neural networks.

---

## 🚀 Features

- Uses a dataset of **6,000 training**, **2,000 test**, and **2,000 validation CAPTCHA images**.
- Employs **ResNet50** (pre-trained on ImageNet) as a feature extractor.
- Predicts **6-character alphanumeric CAPTCHA text** per image.
- Trained using a **regression-based approach with MSE loss**.
- Image preprocessing pipeline handles **variable input sizes**.
- Simple prediction supported for **single-image inference**.
- Model serves as a baseline for further experimentation (e.g., CRNN + CTC).

---

## 🧠 Model Architecture

| Layer Type        | Description                                    |
|-------------------|------------------------------------------------|
| **Base Model**    | `ResNet50` with `include_top=False`, ImageNet weights |
| **Pooling**       | Global Average Pooling 2D                      |
| **Dense Layer 1** | 512 units, Activation: ReLU                    |
| **Dense Layer 2** | 256 units, Activation: ReLU                    |
| **Output Layer**  | 6 units (regression output for character encoding) |

---

## ⚙️ Current Status

- ✅ Implemented using **TensorFlow/Keras**
- 🔧 Basic ResNet-based architecture tested
- 📉 Achieved:
  - Training Loss: `0.0719`
  - Test Loss: `0.1021`
- 🔜 To Do:
  - Automate full prediction pipeline
  - Improve accuracy via better loss functions (CTC)
  - Explore character-wise decoding with CRNN

---
