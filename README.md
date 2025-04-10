# Facial Emotion Recognition System

This project implements a high-performance emotion classification system that achieves 93.98% accuracy using deep learning and machine learning techniques. The system leverages transfer learning with ResNet50 for feature extraction and an SVM classifier for emotion prediction.

## Key Features

- Utilizes transfer learning with pre-trained ResNet50 model
- Optimized for 220×220 pixel input images
- Implements efficient batch processing
- Provides model serialization for easy deployment
- Ensures reproducible results with fixed random seeds

## Technical Specifications

- Python 3.8+
- TensorFlow 2.6+
- scikit-learn 1.0+
- Processes 5 emotion classes: Angry, Happy, Surprise, Fear, Neutral
- Handles 1,477 total images with balanced distribution

## Performance Results

The system demonstrates excellent classification performance:

- Overall accuracy: 93.98%
- Best performing class (Surprise): 98% F1-score
- Most challenging class (Angry): 88% F1-score
- Consistent performance across all emotion categories

## Implementation Details

The pipeline includes:
1. Image preprocessing and feature extraction
2. SVM model training with linear kernel
3. Comprehensive evaluation metrics
4. Model persistence for reuse

## Usage Instructions

To use this system:
1. Prepare your dataset in the specified structure
2. Run the feature extraction script
3. Train the model
4. Evaluate performance
5. Save the trained model for deployment

## Future Enhancements

Potential improvements include:
- Real-time emotion detection
- Web/mobile interface integration
- Additional emotion categories
- Advanced data augmentation techniques

This system provides a robust foundation for facial emotion recognition applications with production-ready capabilities.
