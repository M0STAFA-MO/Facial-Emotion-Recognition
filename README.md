# Facial Emotion Recognition System

This project implements a high-performance emotion classification system that achieves **93.98% accuracy** using deep learning and machine learning techniques. The system leverages transfer learning with ResNet50 for feature extraction and an SVM classifier for emotion prediction.

## Key Features

- **Transfer Learning**: Utilizes pre-trained ResNet50 model (ImageNet)
- **Optimized Input**: 220×220 pixel images for efficient processing
- **Batch Processing**: Efficient GPU/CPU utilization with configurable batch sizes
- **Model Persistence**: Joblib serialization for easy deployment
- **Reproducible**: Fixed random seeds (42) for consistent results

## Technical Stack

| Component | Technology |
|-----------|------------|
| Language | Python 3 |
| Deep Learning | TensorFlow/Keras |
| ML | scikit-learn |
| Feature Extraction | ResNet50 (pre-trained on ImageNet) |
| Classifier | Linear SVM |
| Data Processing | NumPy, tqdm |

## Dataset

The system classifies **5 emotion categories**:

| Emotion | Images |
|---------|--------|
| Angry | 310 |
| Happy | 309 |
| Surprise | 310 |
| Fear | 310 |
| Neutral | 238 |

**Total**: 1,477 images | **Input**: 220×220 RGB

## Performance Results

| Metric | Score |
|--------|-------|
| **Overall Accuracy** | **93.98%** |
| Macro Avg F1-Score | 94% |
| Weighted Avg F1-Score | 94% |

**Per-Class F1-Scores**:
- Surprise: 98%
- Neutral: 97%
- Happy: 95%
- Fear: 93%
- Angry: 88%

## Pipeline Overview

1. **Data Loading** → Count images per emotion class
2. **Feature Extraction** → ResNet50 (pre-trained, no top layers)
3. **Batch Processing** → 220×220 resize + ImageNet preprocessing
4. **Train/Test Split** → 82/18 stratified split
5. **SVM Training** → Linear kernel, random_state=42
6. **Evaluation** → Accuracy + classification report
6. **Model Save** → Joblib serialization

## Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/M0STAFA-MO/Facial-Emotion-Recognition/blob/main/Emotion%20Recognition.ipynb)

```bash
# 1. Open the notebook in Colab
# 2. Runtime → Change runtime type → GPU (T4)
# 3. Run all cells (Ctrl+F9)
# 4. Get 93.98% accuracy 
```

## Google Drive Dataset

Place your dataset at:
```
/content/drive/MyDrive/Colab Notebooks/project/Emotions-Data/
├── Angry/
├── Happy/
├── Surprise/
├── Fear/
└── Neutral/
```

Or download from: [Dataset](https://drive.google.com/drive/folders/1tycCZMfXJexuQQyOFbkgELzR6gPV3sKM?usp=sharing)

## Requirements

```
tensorflow>=2.11
scikit-learn>=1.3
numpy>=1.24
joblib>=1.3
tqdm>=4.65
```

## Future Enhancements

- [ ] Real-time webcam emotion detection
- [ ] Web/mobile interface (Streamlit/Gradio)
- [ ] Additional emotion categories (Disgust, Contempt)
- [ ] Data augmentation for improved generalization
- [ ] Model quantization for edge deployment

## License

MIT License - See LICENSE file for details.

## Acknowledgments

-  Custom dataset
- ResNet50: He et al., "Deep Residual Learning for Image Recognition" (2015)
- Built with TensorFlow, scikit-learn, and ❤️
