Heart Disease Prediction – By Samiha Azeem
Objective

Predict whether a person is at risk of heart disease based on health data using machine learning models. The goal is to provide a simple, interpretable, and accurate predictive tool.

Dataset

Columns / Features:

age – Age of patient
sex – 1 = male, 0 = female
cp – Chest pain type (0–3)
trestbps – Resting blood pressure (mm Hg)
chol – Serum cholesterol (mg/dl)
fbs – Fasting blood sugar > 120 mg/dl (1 = true; 0 = false)
restecg – Resting electrocardiographic results (0–2)
thalach – Maximum heart rate achieved
exang – Exercise-induced angina (1 = yes; 0 = no)
oldpeak – ST depression induced by exercise relative to rest
slope – Slope of the peak exercise ST segment (0–2)
ca – Number of major vessels colored by fluoroscopy (0–3)
thal – Thalassemia (1 = normal; 2 = fixed defect; 3 = reversible defect)

Target:

target – 1 = presence of heart disease, 0 = absence of heart disease

Source: UCI Heart Disease Dataset (available on Kaggle)

Methodology

1. Data Exploration & Cleaning

Checked for missing values; no cleaning required.
Visualized target distribution and feature correlations.

2. Preprocessing

Split dataset into train (80%) and test (20%) sets.
Scaled features for Logistic Regression.

3. Models

Logistic Regression: interpretable, outputs probability of disease.
Decision Tree: captures non-linear relationships, provides feature importance.

4. Evaluation Metrics

Accuracy
Confusion Matrix
ROC Curve & AUC

Feature Importance Analysis

Results
Model	                        Accuracy	            ROC-AUC
Logistic Regression	            0.852	                0.91
Decision Tree	                  0.852	                0.88

Observations:

Both models perform similarly (~85% accuracy).
Logistic Regression is easier to interpret via coefficients.
Decision Tree highlights the most important features for splitting.
Top features across models: cp (chest pain), oldpeak (ST depression), ca (number of vessels).

Feature Importance

Logistic Regression (Top features): cp, slope, thalach
Coefficients indicate the direction of impact on disease risk.
Decision Tree (Top features): cp, ca, oldpeak, exang, age
Feature importance shows how much a feature contributes to splitting decisions.

ROC Curve: ROC (Receiver Operating Characteristic) plots the True Positive Rate (TPR) vs False Positive Rate (FPR) across thresholds.

AUC (Area Under Curve) measures overall model performance (closer to 1 = better).
ROC curves are useful for imbalanced datasets like medical data.

Exploratory Data Analysis (EDA)

Target distribution shows a balance between disease and no disease.
Correlation heatmap helps identify influential features.
Strongest predictors: cp, oldpeak, ca, exang.
