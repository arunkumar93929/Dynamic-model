# Hybrid CIFAR-10 Image Classification Model

This project implements a hybrid model for image classification on the CIFAR-10 dataset. The model combines a Decision Tree and a Convolutional Neural Network (CNN) to optimize prediction accuracy and reduce computational load on the CNN by deferring confident predictions to the Decision Tree. This approach improves efficiency by only relying on the CNN for uncertain classifications, based on a configurable confidence threshold.

## Project Structure

1. **Data Loading and Preprocessing**: Loads and normalizes the CIFAR-10 dataset and extracts basic statistical features from images for the Decision Tree model.
2. **Decision Tree Model**: Trains a calibrated Decision Tree model using basic image features for initial classification.
3. **CNN Model**: Constructs and trains a CNN model with data augmentation to improve classification accuracy.
4. **Hybrid Model**: Combines predictions from the Decision Tree and CNN. For uncertain predictions (below a confidence threshold), the model defers to the CNN.
5. **Performance Evaluation**: Evaluates the accuracy and prediction time of both the CNN and the hybrid model. Calculates the reduction in CNN load achieved by the hybrid approach.

## Requirements

Ensure the following dependencies are installed:
- `numpy`
- `tensorflow`
- `scikit-learn`

To install the necessary packages, run:
```bash
pip install numpy tensorflow scikit-learn
