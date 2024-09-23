# Supervised-Machine-Learning-Project-2-


# Breast Cancer Classification with Logistic Regression

## 1. Overview

This project implements a Logistic Regression model for classifying breast cancer as **benign (B)** or **malignant (M)** using features extracted from digitized images of fine needle aspirates (FNAs) of breast masses. The dataset is part of the Breast Cancer Wisconsin (Diagnostic) Dataset.

## 2. Dataset Description

The dataset consists of 569 samples of breast mass tissue, each described by 30 features derived from images. These features are numerical and describe the characteristics of the cell nuclei present in the image.

- **Source**: Breast Cancer Wisconsin (Diagnostic) dataset.
- **Number of Samples**: 569
- **Number of Features**: 32 (including the `diagnosis` label)

### 2.1. Features

The dataset includes the following features, each computed for three different statistics (mean, standard error, and worst-case):
- **Radius**
- **Texture**
- **Perimeter**
- **Area**
- **Smoothness**
- **Compactness**
- **Concavity**
- **Concave points**
- **Symmetry**
- **Fractal dimension**

### 2.2. Target Variable

- **Diagnosis**: Binary classification target:
  - **Malignant (M)**: Coded as `1`
  - **Benign (B)**: Coded as `0`


## 3. Conclusion

This project demonstrates how logistic regression can be applied to the problem of breast cancer diagnosis. The model achieved a high accuracy, making it a suitable method for this binary classification problem. The confusion matrix and prediction plot provide further insights into the model's performance.

## 4. Future Work

- Experiment with different machine learning models (e.g., Decision Trees, Support Vector Machines).
- Tune hyperparameters of the logistic regression model to potentially improve accuracy.
- Explore feature selection techniques to identify the most important features for breast cancer classification.

