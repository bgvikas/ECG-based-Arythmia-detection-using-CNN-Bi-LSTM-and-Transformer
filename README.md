# 🫀 Cardiac Arrhythmia Detection Using a Hybrid Bi-LSTM–Transformer Model

## 📌 Overview
Cardiac arrhythmia is a condition in which the heart beats irregularly — too fast, too slow, or with an abnormal rhythm.  
Early detection and classification of arrhythmias is crucial for **timely diagnosis and prevention of cardiovascular diseases**.  

This project proposes a **hybrid deep learning approach** that integrates:
- **Convolutional Neural Networks (CNNs)** for local feature extraction,
- **Bidirectional LSTMs (Bi-LSTMs)** for learning temporal dependencies, and
- **Transformer Encoders** for modeling long-range dependencies using self-attention.  

The model is trained and evaluated on the **MIT-BIH Arrhythmia Dataset** and achieves **97% classification accuracy**, demonstrating its potential as a clinical decision-support tool.  

---

## 🎯 Objectives
- To preprocess ECG signals for noise reduction and normalization.  
- To design a **hybrid CNN + Bi-LSTM + Transformer model** that improves upon traditional deep learning approaches.  
- To classify arrhythmias with **high accuracy and robustness**.  
- To evaluate performance using **multiple metrics** (Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC Curve).  
- To provide visualizations for better interpretability of the results.  

---

## 🗂 Dataset
- **Dataset Used:** MIT-BIH Arrhythmia Database  
- **Details:**  
  - 48 half-hour ECG recordings from 47 subjects.  
  - Sampling frequency: 360 Hz.  
  - Annotated with heartbeat types (Normal, Ventricular ectopic, Supraventricular ectopic, Fusion beats, Unknown beats).  

---

## 🏗 Methodology

### 🔹 1. Data Preprocessing
- Signal normalization  
- Noise removal using band-pass filtering  
- Segmentation into heartbeat intervals  
- Label encoding for arrhythmia classes  

### 🔹 2. Model Architecture
1. **CNN Layers**  
   - Extract low-level features from ECG signals (morphological patterns).  

2. **Bi-LSTM**  
   - Capture sequential dependencies in both forward and backward directions.  

3. **Transformer Encoder**  
   - Self-attention mechanism to learn **global dependencies** and contextual features.  

4. **Dense Layers + Softmax**  
   - Fully connected layers for classification into arrhythmia categories.  

### 🔹 3. Training
- Loss Function: `categorical_crossentropy`  
- Optimizer: `Adam`  
- Epochs: Tuned for optimal accuracy  
- Batch Size: Configurable  

### 🔹 4. Evaluation
- Accuracy  
- Precision, Recall, F1-score  
- Confusion Matrix  
- ROC Curve & AUC  

---

## ⚙️ Installation

### 🔹 Clone the repository
```bash
git clone https://github.com/your-username/Cardiac-Arrhythmia-Detection.git
cd Cardiac-Arrhythmia-Detection
