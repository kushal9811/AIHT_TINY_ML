# Vibration-Based Anomaly Detection Using Mahalanobis Distance and Multi-Head Attention Autoencoder

## 📌 Project Overview

This project focuses on detecting anomalies in vibration signals using a combination of traditional statistical techniques and deep learning. We first apply Mahalanobis distance for anomaly detection using statistical properties. Then, we implement a basic autoencoder to learn the reconstruction of normal signals. To improve performance, we extend it using a *Multi-Head Attention Autoencoder (MHA-AE)*, which dynamically attends to important features for robust and adaptive anomaly detection.

## 🔍 Motivation

Vibration signals from mechanical systems often carry rich information about the health of the system. Subtle changes in vibration patterns may indicate potential faults. Traditional methods struggle with subtle anomalies or noisy data. Our hybrid approach aims to combine statistical efficiency with deep learning generalization to improve detection performance, especially in edge deployment scenarios.

---

## 🧠 Techniques Used

- *Mahalanobis Distance* – For statistical anomaly detection.
- *Basic Autoencoder* – For unsupervised learning of normal patterns.
- *Multi-Head Attention Autoencoder* – For better generalization, dynamic feature weighting, and lower false positives.
- *Reconstruction Loss (MSE)* – Used to detect anomalies when loss exceeds a learned threshold.
- *Optimizers* – Adam, RMSprop tested.
- *Regularization* – Dropout layers were added and tuned to prevent overfitting.

---

## 🏗 Architecture

### Mahalanobis-Based Detector
- Calculates mean and covariance from normal data.
- Computes Mahalanobis distance to classify anomalies.

### Basic Autoencoder
- Encoder → Bottleneck → Decoder
- Learns to reconstruct only normal signals.
- Anomalies result in high reconstruction error.

### Multi-Head Attention Autoencoder (MHA-AE)
1. *Input Layer* – Raw or preprocessed vibration features.
2. *Encoder with Multi-Head Attention* – Focuses on critical features.
3. *Bottleneck (Latent Space)* – Compressed meaningful representation.
4. *Decoder* – Attempts to reconstruct original input.
5. *Loss Function* – MSE is used to compute reconstruction error.
6. *Anomaly Detection* – Samples with error above adaptive threshold are marked anomalous.

---

## 📊 Dataset

- *Type*: Vibration sensor signal data (synthetic or real)
- *Format*: CSV or time-series format
- *Note*: Placeholder dataset used in this repo. Replace with your sensor data for deployment.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/vibration-anomaly-mha-autoencoder
   cd vibration-anomaly-mha-autoencoder
