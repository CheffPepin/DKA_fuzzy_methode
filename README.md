# 🍷 White Wine Quality Prediction Using Fuzzy Logic

## Overview

This project implements a **Fuzzy Logic System** to predict the quality of white wine based on its physicochemical properties. Instead of using traditional machine learning models, this project utilizes fuzzy inference to model human-like reasoning in evaluating wine quality.

The project includes:

* Data preprocessing
* Fuzzy membership function design
* Fuzzy rule creation
* Fuzzy inference process
* Defuzzification
* Model evaluation using classification accuracy


## Dataset

The dataset used is the **White Wine Quality Dataset** from the UCI Machine Learning Repository.

### Features

| Feature              | Description                        |
| -------------------- | ---------------------------------- |
| Fixed Acidity        | Tartaric acid concentration        |
| Volatile Acidity     | Acetic acid concentration          |
| Citric Acid          | Citric acid concentration          |
| Residual Sugar       | Remaining sugar after fermentation |
| Chlorides            | Salt concentration                 |
| Free Sulfur Dioxide  | Free SO₂ concentration             |
| Total Sulfur Dioxide | Total SO₂ concentration            |
| Density              | Density of wine                    |
| pH                   | Acidity level                      |
| Sulphates            | Potassium sulphate concentration   |
| Alcohol              | Alcohol percentage                 |

**Target Variable**

* Quality (score from 0–10)

## Project Pipeline

Dataset
     │
     ▼
Data Preprocessing
- Handle missing values
- Feature selection
- Normalization (optional)
     │
     ▼
Define Membership Functions
- Low
- Medium
- High
     │
     ▼
Build Fuzzy Rules
Example:
IF Alcohol is High
AND Volatile Acidity is Low
THEN Wine Quality is High
     │
     ▼
Fuzzy Inference System
(Mamdani)
     │
     ▼
Defuzzification
(Centroid Method)
     │
     ▼
Predicted Quality
     │
     ▼
Performance Evaluation
- Accuracy
- Confusion Matrix

## Fuzzy System

### Input Variables

The fuzzy system uses selected physicochemical attributes as input variables, such as:

* Alcohol
* Volatile Acidity
* Sulphates
* Density
* pH

Each variable is represented by three linguistic terms:

* Low
* Medium
* High

### Output Variable

Wine Quality is classified into:

* Low Quality
* Medium Quality
* High Quality

---

## Fuzzy Rules

Example rules:

* IF Alcohol is **High** AND Volatile Acidity is **Low**, THEN Quality is **High**
* IF Alcohol is **Low** AND Density is **High**, THEN Quality is **Low**
* IF Sulphates are **Medium** AND pH is **Medium**, THEN Quality is **Medium**

The complete rule base is implemented in the source code.

---

## Model Evaluation

The fuzzy model performance is evaluated using classification accuracy.

**Accuracy Formula**

[
Accuracy = \frac{Number\ of\ Correct\ Predictions}{Total\ Predictions} \times 100%
]

Additional evaluation may include:

* Confusion Matrix
* Precision
* Recall
* F1-score

## Project Structure

├── dataset/
│   └── winequality-white.csv
│
├── notebooks/
│   └── fuzzy_white_wine.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── membership.py
│   ├── rules.py
│   └── inference.py
│
├── results/
│   ├── confusion_matrix.png
│   └── accuracy.png
│
└── README.md

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Fuzzy
* Scikit-Learn
* Matplotlib

## Results

The fuzzy inference system successfully predicts wine quality based on selected physicochemical attributes.

**Model Accuracy:** 53.18% - 77.99%

## Future Improvements

* Optimize membership function parameters.
* Expand the fuzzy rule base.
* Compare fuzzy logic with machine learning models such as Decision Tree, Random Forest, and XGBoost.
* Implement automatic rule optimization using evolutionary algorithms.
