# Brain Tumor Classification using CNN

This project implements a Deep Learning model to classify Brain MRI images into two categories: Tumor and Normal. It utilizes a Convolutional Neural Network (CNN) built with Keras and TensorFlow to achieve high diagnostic accuracy.

### Project Overview

The primary goal of this notebook is to automate the detection of brain tumors from MRI scans. The pipeline includes data preprocessing, image resizing, one-hot encoding of labels, and a customized CNN architecture featuring Batch Normalization and Dropout layers for stability and performance.

### Dataset

The project uses the Brain MRI Images for Brain Tumor Detection dataset.

Classes:
0: Tumor
1: Normal

Preprocessing: Images are resized to 128x128 pixels and converted into NumPy arrays for model consumption.

Split: The data is split into 80% training and 20% testing sets using train_test_split.

### Model Architecture

The model is a Sequential CNN designed to extract hierarchical features from MRI scans:

| Layer Type | Configuration |
| :--- | :--- |
| **Convolutional** | 32 filters (2x2), ReLU activation |
| **Convolutional** | 32 filters (2x2), ReLU activation |
| **Normalization** | Batch Normalization |
| **Pooling** | MaxPooling (2x2) |
| **Regularization** | Dropout (25%) |
| **Convolutional** | 64 filters (2x2), ReLU activation |
| **Convolutional** | 64 filters (2x2), ReLU activation |
| **Normalization** | Batch Normalization |
| **Pooling** | MaxPooling (2x2) |
| **Dense (Hidden)** | 512 units, ReLU activation |
| **Regularization** | Dropout (50%) |
| **Output** | 2 units, Softmax activation |

### Training Process
Loss Function: Categorical Crossentropy.

Optimizer: Adamax.

Feature Highlights: The inclusion of Batch Normalization helps stabilize the learning process and reduces the number of training epochs required for convergence.

### Technologies Used
Deep Learning: Keras, TensorFlow.

Image Processing: PIL (Pillow).

Data Science: NumPy, Pandas, Scikit-learn.

Visualization: Matplotlib.

### How to Run

1. Ensure the dataset is located in the path: ../input/brain-mri-images-for-brain-tumor-detection/.

2. Install dependencies:

```Bash

pip install keras tensorflow pillow numpy pandas scikit-learn matplotlib
```
3. Run the notebook brain-tumor-classification.ipynb.
