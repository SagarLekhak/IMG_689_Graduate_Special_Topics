This directory contains project related to classification and regression of hyperspectral imaging data and regression of multispectral data. The codes can be duplicated for any hyperspectral or multispectral data. The projects are divided into two main categories: Classification and Regression. The classification project is further divided into two tasks: Binary Classification and Multi-Class Classification using XGBoost. The regression project is divided into three tasks: Linear Regression, Partial Least Squares Regression (PLSR), and Multi-Layer Perceptron (MLP) Regression.

# 1. Classification
- Dataset: Pavia University
- Description: Hyperspectral image dataset collected by the ROSIS-3 sensor over Pavia, Italy.

- Dimensions: 
610
×
340
610×340 pixels with 103 spectral bands.

- Classes: 9 classes (imbalanced dataset).

### Task 1 : Binary Classification of Vegetation and Non-Vegetation pixels.
- Exploratory Data Analysis (EDA): Analyze the dataset to understand its structure, class distribution, and spectral characteristics.
Identify key aspects to explore before modeling.

- Balance the dataset by undersampling or oversampling.

- Binary Classification (Logistic Regression):
Distinguish between Vegetation (trees and meadows) and Non-vegetation (all other classes).

### Steps:

- Generate training and testing partitions.

- Ensure equal representation of original 9 classes in the binary problem.

- Select bands in the blue, green, red, red-edge, and near-infrared regions.

- Preprocess the data.

- Compute and report metrics: Mean Accuracy, Mean Per-Class Accuracy, Precision, Recall, F1-Score.

- Plot the ROC curve and compute AUC.

- Interpret findings.

### Task 2 : Multi-Class Classification (XGBoost): Classify all 9 classes using XGBoost.

- Use XGBoost for multi-class classification.

### Steps:

- Generate balanced training and testing partitions.

- Use 5 selected bands (or more if needed).

- Preprocess the data.

- Train XGBoost and analyze performance.

- Generate feature importance plots and confusion matrix.

- Report metrics: Mean Accuracy, Mean Per-Class Accuracy, Precision, Recall, F1-Score.

- Compare performance with and without data balancing.

- Discuss findings.

# Problem 2: Regression
- Dataset: Landis Chlorophyll
- Description: Simulated dataset combining PROSPECT and MODTRAN models for chlorophyll content prediction.

- Dimensions: 1000 samples with 10 spectral bands.

### Task 1 : Predict chlorophyll content using linear regression(LR).
- Exploratory Data Analysis (EDA):
Analyze the dataset to understand its structure, feature correlations, and target variable distribution.

- Check for multicollinearity and class balance.

- Linear Regression:
Predict chlorophyll content using linear regression.

### Steps:

- Preprocess the data.

- Split the dataset into training and testing sets.

- Train the model and report metrics: MAE, R², Standard Deviation of Residuals.

- Generate regression and residual plots.

- Analyze trends and interpret findings.

- Partial Least Squares Regression (PLSR):

### Task 2 : Use Partial Least Square Regression (PLSR) to predict chlorophyll content.

### Steps:

- Vary the number of components from 1 to 10.

- Identify the best-performing component count.

- Generate regression and residual plots for the best model.

- Compare trends with linear regression and interpret findings.

### Task 3 : Predict Chlorophyll content using Multi-Layer Perceptron (MLP) Regression:

- Use MLP with varying numbers of hidden layers (1-5) and ReLU activation.

### Steps:

- Train MLP models with different complexities.

- Generate regression and residual plots for each model.

- Report evaluation metrics (MAE, R², Standard Deviation of Residuals).

- Analyze trends in residual plots.

- Compare performance with Linear Regression and PLSR.

- Discuss bias-variance tradeoff and interpret findings.

