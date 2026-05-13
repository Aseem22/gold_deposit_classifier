# Gold Deposit Type Classification using Trace Element Geochemistry

## Overview

This project applies Machine Learning and Geochemical Data Analysis techniques to classify different types of gold deposits using pyrite trace element data.

The workflow includes:

* Data preprocessing and cleaning
* Missing value analysis
* Multiple imputation techniques
* Exploratory Data Analysis (EDA)
* Compositional Data Transformation (CLR)
* Principal Component Analysis (PCA)
* Interactive visualizations
* Machine Learning model training and evaluation

The project was developed as part of research work focused on understanding how trace element signatures in pyrite can help identify and classify gold deposit types.

---

# Project Objectives

The main objective of this project is to:

* Predict gold deposit types using trace element concentrations
* Handle missing geochemical data effectively
* Compare multiple imputation approaches
* Identify important geochemical features
* Visualize relationships between trace elements
* Build robust classification models for geological interpretation

---

# Dataset Description

The dataset contains geochemical trace element concentrations measured in pyrite samples.

### Features Include:

* Co (ppm)
* Ni (ppm)
* Cu (ppm)
* Zn (ppm)
* As (ppm)
* Se (ppm)
* Mo (ppm)
* Ag (ppm)
* Sb (ppm)
* Te (ppm)
* Au (ppm)
* Pb (ppm)
* Bi (ppm)
* Tl (ppm)
* Mn (ppm)
* V (ppm)

### Target Variable

`Deposit type`

Represents different classes of gold deposits.

---



## 2. Statistical Summary Analysis

The project computes grouped summary statistics for each deposit type.

### Statistics Calculated

* Minimum
* Maximum
* Mean
* Standard Deviation
* Coefficient of Variation (CV)

## 3. Missing Value Imputation

Geochemical datasets often contain missing or censored values.

### Imputation Methods Used

#### KNN Imputation

Uses nearest neighboring samples to estimate missing values.

```python
KNNImputer(n_neighbors=5)
```

#### Mean Imputation

Replaces missing values using the column mean.

#### Iterative Imputation (MICE)

Predicts missing values iteratively using other features.

### Statistical Validation

The imputed datasets are statistically evaluated using:

* Kolmogorov–Smirnov Test
* Chi-Square Tests


<img width="739" height="390" alt="image" src="https://github.com/user-attachments/assets/0bcc6531-d609-4c19-806d-c00d5e00605c" />


---

## 4. CLR Transformation

Because geochemical data is compositional in nature, the project applies:

# Centered Log Ratio (CLR) Transformation

CLR transformation helps:

* Normalize compositional relationships
* Reduce bias
* Improve machine learning performance

### Transformation

```python
clr_transformed = log_values.subtract(log_values.mean(axis=1), axis=0)
```

---

## 5. Principal Component Analysis (PCA)

* Dimensionality reduction
* Identifying dominant geochemical signatures
* Understanding variance structure in the data
* Detects important trace elements
* Visualizes clustering patterns
* Simplifies high-dimensional data

<img width="780" height="590" alt="image" src="https://github.com/user-attachments/assets/451eeb87-1060-477a-b76b-ba5221bd465b" />
<img width="790" height="490" alt="image" src="https://github.com/user-attachments/assets/e2c89dcc-b0e0-40b6-8f60-e797c9c4b219" />


---

## 6. Exploratory Data Analysis (EDA)

### Box Plots

### Scatter Plots

* Element relationships
* Clustering patterns
* Outliers
* Deposit-specific geochemical trends


---

# Machine Learning Models

The final stage of the project trains classification models.

## Models Used

### Random Forest Classifier

### Gradient Boosting Classifier

### Support Vector Machine (SVM)

### Bagging Classifier

### Stacking Classifier

Combines multiple models for improved performance.

---

# Model Evaluation

The models were evaluated using:

* Accuracy Score
* Classification Report
* Confusion Matrix
* Precision, Recall, and F1-score


---


## Feature Importance


# Key Geological Insights

This project demonstrates how machine learning can assist geological exploration by:

* Identifying deposit-specific geochemical signatures
* Reducing manual interpretation effort
* Improving mineral exploration workflows
* Supporting data-driven exploration strategies

Trace element signatures in pyrite can provide valuable information about:

* Ore-forming environments
* Hydrothermal processes
* Deposit genesis

---

# Dataset Availability

The dataset used in this project was provided for academic research purposes and is not publicly available due to data confidentiality and ownership restrictions.

However, the complete preprocessing workflow, feature engineering pipeline, statistical analysis, visualizations, and machine learning methodology are fully documented in this repository.

---

# Why I Built This Project

This project was developed as part of my research work in Applied Geology to explore how machine learning can be used in mineral exploration.

Gold deposit classification using trace element geochemistry is often difficult because geological data is noisy, high-dimensional, and contains many missing values. Through this project, I wanted to understand how statistical analysis and machine learning techniques can help identify meaningful patterns in geochemical datasets.

The project combines concepts from:

* Economic Geology
* Geochemistry
* Data Science
* Machine Learning

---


