# Road Accident Detection Using Deep Learning from Traffic Camera Images

## Project Overview

This project focuses on automatic road accident detection using deep learning and traffic camera images. The goal is to classify road images into two categories:

- Accident
- No Accident

The project uses supervised image classification techniques and compares different machine learning and deep learning models for accident detection.

---

# Problem Statement

Road accidents are a major public safety issue and delayed detection can increase emergency response time and damage severity.

The objective of this project is to build a deep learning system that can automatically detect accidents from traffic surveillance images.

Input:
- RGB traffic camera image

Output:
- Accident
- No Accident

This system can support:
- Smart traffic monitoring
- Faster emergency response
- Automated surveillance systems
- Road safety improvement

---

# Dataset

The dataset contains traffic scene images divided into two folders:

```text
Accident
No_Accident
```

Each image represents a real-world road scenario captured using traffic cameras.

Dataset characteristics:
- Binary image classification
- Different lighting conditions
- Different camera angles
- Real traffic scenes

Sample dataset location:

```text
data/sample/
```

Folder structure:

```text
data/sample/Accident/
data/sample/No_Accident/
```

---

# Data Preprocessing

The following preprocessing steps are applied:

- Image resizing to 224 × 224
- Tensor conversion
- Data loading using PyTorch ImageFolder

Optional augmentations discussed:
- Horizontal flip
- Rotation
- Brightness adjustment

---

# Models Used

This project includes the following models:

## 1. Logistic Regression (Baseline)

A classical machine learning baseline where images are flattened into feature vectors.

Purpose:
- Baseline comparison
- Simpler non-deep learning approach

---

## 2. Convolutional Neural Network (CNN)

A simple CNN architecture is used to learn spatial image features such as:
- edges
- shapes
- object patterns

Purpose:
- Improve feature learning over traditional ML

---

## 3. ResNet-18 (Primary Model)

ResNet-18 is the primary deep learning model used in this project.

Features:
- Residual connections
- Transfer learning using ImageNet weights
- Better optimization for deep networks

Purpose:
- Achieve higher classification performance
- Improve generalization

---

# Experimental Setup

Train/Test Split:
- 70% Training
- 15% Validation
- 15% Testing

Training Details:
- Loss Function: Cross Entropy Loss
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 4
- Epochs: 2 (demo version)

Frameworks Used:
- PyTorch
- Torchvision
- Scikit-learn
- Pandas
- Matplotlib

---

# Evaluation Metrics

The following evaluation metrics are used:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Recall and F1-score are important because missing accident detection can be dangerous in real-world systems.

---

# Results

The trained model generates:

- metrics.csv
- confusion_matrix.png
- loss_curve.png

Results location:

```text
outputs/results/
outputs/figures/
```

---

# Failure Analysis

The model may struggle in:
- Low-light conditions
- Heavy traffic congestion
- Motion blur
- Occluded vehicles

These limitations show the importance of:
- Larger datasets
- Better augmentation
- Video-based modeling

---

# Ethics and Responsible Use

This project raises several ethical considerations:

- False negatives may delay emergency response
- False positives may waste resources
- Surveillance systems must respect privacy
- Dataset bias may affect performance

The system should be used as a decision-support tool rather than a fully autonomous safety system.

---

# Project Structure

```text
SP25-690-Meka/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── sample/
│       ├── Accident/
│       └── No_Accident/
│
├── notebooks/
│   └── accident_detection_demo.ipynb
│
├── outputs/
│   ├── results/
│   │   └── metrics.csv
│   │
│   └── figures/
│       ├── confusion_matrix.png
│       └── loss_curve.png
│
├── models/
│
└── reports/
```

---

# How to Run the Project

## Step 1: Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Step 2: Open Google Colab

Open:

```text
https://colab.research.google.com/
```

Upload the notebook:

```text
notebooks/accident_detection_demo.ipynb
```

---

## Step 3: Upload Dataset

Upload the sample dataset zip file containing:

```text
Accident/
No_Accident/
```

---

## Step 4: Run the Notebook

Run all notebook cells sequentially.

The notebook will:
- Load the dataset
- Train ResNet-18
- Evaluate performance
- Generate output files

---

## Step 5: Output Files

Generated output files:

```text
metrics.csv
confusion_matrix.png
loss_curve.png
```

---

# Dependencies

The project uses:

```text
torch
torchvision
numpy
pandas
matplotlib
scikit-learn
Pillow
tqdm
```

---

# Future Work

Possible future improvements include:

- Video-based accident detection
- CNN-LSTM models
- Transformer architectures
- Real-time deployment
- Larger datasets
- Explainable AI methods such as Grad-CAM

---

# References

- Goodfellow, Bengio, Courville — Deep Learning
- Prince — Understanding Deep Learning
- He et al. — Deep Residual Learning for Image Recognition
- PyTorch Documentation
- Kaggle Traffic Accident Datasets
