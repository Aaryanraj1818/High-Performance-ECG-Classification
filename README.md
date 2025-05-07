# High Performance Cardiovascular Signal Classification System

This repository contains MATLAB scripts and functions developed for my final year project: a deep learning-based ECG signal classification system using time-frequency representations.

## 📌 Project Overview

The goal of this project is to classify ECG signals into three cardiac conditions using convolutional neural networks trained on RGB images generated from ECG signals.

### Classification Categories:
- **Arrhythmia (ARR)**
- **Congestive Heart Failure (CHF)**
- **Normal Sinus Rhythm (NSR)**

## 🔍 Methodology

1. **Signal Preprocessing:**
   - ECG signals obtained from PhysioNet.
   - Each recording contains 65,536 samples.
   - Divided into chunks of 500 samples.
   - 30 recordings per class selected for balanced data.

2. **Time-Frequency Transformation:**
   - Continuous Wavelet Transform (CWT) applied to each signal chunk.
   - CWT results converted into RGB images using the `jet` colormap.

3. **Model Training:**
   - Deep learning performed using pretrained CNNs:
     - **AlexNet** (Transfer Learning)
     - **SqueezeNet**
   - Training and validation done using MATLAB’s Deep Learning Toolbox.

## 📊 Dataset Summary

| Class | #Recordings | #Images |
|-------|-------------|---------|
| ARR   | 30          | 600     |
| CHF   | 30          | 600     |
| NSR   | 30          | 600     |

- **Total images:** 1800 (600/class)
- **Split:** 80% Training, 20% Validation

## 🧠 Results

| Model      | Validation Accuracy |
|------------|---------------------|
| AlexNet    | 98.33%              |
| SqueezeNet | 97.57%           |

## 📁 Folder Structure
physionet_ECG_data-main/
├── ECGData.mat
├── Code/
├── CWT_Images/
└── Models/

## 👤 Author
Aaryan Raj - Department of Computer Science & Engineering  
National Institute of Technology, Calicut
