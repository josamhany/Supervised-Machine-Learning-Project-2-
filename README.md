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

### 2.3. Data Cleaning

The dataset contains an unnecessary column, `Unnamed: 32`, which was removed before processing. Additionally, the diagnosis column was mapped from categorical values ('M' and 'B') to numerical values (`1` and `0`).

## 3. Logistic Regression Model

### 3.1. Preprocessing

The dataset was split into **training** and **testing** sets (80% training and 20% testing) to assess the model's performance on unseen data.

- **Feature Scaling**: To ensure that all features contribute equally to the model, standardization was applied using `StandardScaler`, which transformed the features to have a mean of 0 and a standard deviation of 1.

### 3.2. Model Training

A logistic regression model was trained on the standardized training set. Logistic regression is a linear model for binary classification, which estimates the probability of the binary target being `1` (Malignant) using a logistic (sigmoid) function.

- **Algorithm**: Logistic Regression (using `scikit-learn`)
- **Solver**: The default solver (`lbfgs`) was used for optimization.
- **Max Iterations**: By default, the model runs for up to 100 iterations.

### 3.3. Model Evaluation

The model was evaluated on both the training set and the testing set to determine its performance.

#### 3.3.1. Metrics

- **Accuracy**: The ratio of correct predictions to the total number of predictions made.
- **Confusion Matrix**: A table showing the true positive, true negative, false positive, and false negative predictions, which helps visualize the model's performance on different types of errors.

#### 3.3.2. Results

- **Training Accuracy**: The percentage of correct predictions on the training set.
- **Test Accuracy**: The percentage of correct predictions on the testing set.

A confusion matrix was plotted using `seaborn` to help visualize the model's performance.

### 3.4. Prediction Plot

To provide a more detailed view of the model's performance, a plot was created comparing the **actual** vs **predicted** labels for the test set. This helps to see how well the model performs on individual test cases.

## 4. Conclusion

This project demonstrates how logistic regression can be applied to the problem of breast cancer diagnosis. The model achieved a high accuracy, making it a suitable method for this binary classification problem. The confusion matrix and prediction plot provide further insights into the model's performance.

## 5. Future Work

- Experiment with different machine learning models (e.g., Decision Trees, Support Vector Machines).
- Tune hyperparameters of the logistic regression model to potentially improve accuracy.
- Explore feature selection techniques to identify the most important features for breast cancer classification.

