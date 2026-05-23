# MNIST-Handwritten-Digit-Classification

This project compares the performance of three different machine learning / deep learning models on the **MNIST handwritten digit dataset**:

- Perceptron (Single-layer neural network)
- Artificial Neural Network (ANN)
- Convolutional Neural Network (CNN)

The goal is to analyze how model complexity affects classification accuracy on image data.

---

## Dataset

- Dataset: MNIST Handwritten Digits
- Images: 28x28 grayscale images
- Classes: 10 digits (0–9)
- Each image is flattened into 784 features for training classical models

---

## Models Implemented

### 1. Perceptron (Baseline Model)
- Input: Flattened 28×28 images
- Architecture: Single Dense layer (Softmax)
- Optimizer: SGD
- Loss: Categorical Crossentropy

---

### 2. Artificial Neural Network (ANN)
- Input: Flattened images
- Architecture:
  - Dense(128, ReLU)
  - Dense(64, ReLU)
  - Dense(10, Softmax)
- Optimizer: Adam
- Better feature learning than Perceptron

---

### 3. Convolutional Neural Network (CNN)
- Input: 28×28×1 images
- Architecture:
  - Conv2D (32 filters)
  - MaxPooling2D
  - Conv2D (64 filters)
  - MaxPooling2D
  - Flatten
  - Dense(128, ReLU)
  - Dropout(0.5)
  - Dense(10, Softmax)
- Best for image feature extraction

---

## Results

| Model        | Test Accuracy |
|--------------|--------------|
| Perceptron   | ~86%         |
| ANN          | ~94%         |
| CNN          | ~97%         |

CNN performs best due to spatial feature extraction.

---

## Libraries Used

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---
