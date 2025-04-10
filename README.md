# Facial Emotion Recognition System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.6%2B-orange)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-green)
![Accuracy](https://img.shields.io/badge/Accuracy-93.98%25-brightgreen)

A high-performance emotion classification system achieving **93.98% accuracy** using ResNet50 feature extraction and SVM classification.

## Table of Contents
- [Features](#-key-features)
- [Installation](#-installation)
- [Usage](#-usage)
- [Dataset](#-dataset-structure)
- [Performance](#-performance-metrics)
- [Saving/Loading](#-model-persistence)
- [Contributing](#-contributing)

## 🚀 Key Features
- **Transfer Learning**: Leverages pre-trained ResNet50 for efficient feature extraction
- **Optimized Architecture**: Custom 220×220 input size balances accuracy and speed
- **Production-Ready**: Includes model serialization for deployment
- **Reproducible**: Fixed random seeds ensure consistent results
- **Efficient Processing**: Batch image handling with progress tracking

## 💻 Installation
```bash
git clone https://github.com/yourusername/emotion-recognition.git
cd emotion-recognition


📦 dataset/
├── Angry/        # 310 images (220×220 RGB)
├── Happy/        # 309 images 
├── Surprise/     # 310 images
├── Fear/         # 310 images
└── Neutral/      # 238 images

📊 Performance Metrics
Emotion	Precision	Recall	F1-Score
Angry	0.91	0.86	0.88
Happy	0.93	0.96	0.95
Fear	0.93	0.93	0.93
Neutral	0.95	0.98	0.97
Surprise	0.98	0.98	0.98

