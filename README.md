Heart Disease Prediction - By Samiha Azeem

Objective:
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
exang – Exercise induced angina (1 = yes; 0 = no)
oldpeak – ST depression induced by exercise relative to rest
slope – Slope of the peak exercise ST segment (0–2)
ca – Number of major vessels colored by fluoroscopy (0–3)
thal – Thalassemia (1 = normal; 2 = fixed defect; 3 = reversable defect)

Target:

target – 1 = presence of heart disease, 0 = absence of heart disease

Source: UCI Heart Disease Dataset (available on Kaggle)

Methodology

Data Exploration & Cleaning

Checked for missing values; no cleaning required.

Visualized target distribution and correlations.

Preprocessing

Split dataset into train (80%) and test (20%) sets.

Scaled features for Logistic Regression.

Models

Logistic Regression: interpretable, outputs probability of disease.

Decision Tree: captures non-linear relationships, shows feature importance.

Evaluation Metrics

Accuracy

Confusion Matrix

ROC Curve & AUC

Feature Importance Analysis

Results
Model	Accuracy	ROC-AUC
Logistic Regression	0.852	0.91
Decision Tree	0.852	0.88

Observations:

Both models perform similarly in terms of accuracy (~85%).

Logistic Regression is easier to interpret via coefficients.

Decision Tree highlights most important features for splitting.

Chest pain (cp), ST depression (oldpeak), and number of vessels (ca) are top features in both models.

Feature Importance

Logistic Regression (Top features): cp, slope, thalach
Decision Tree (Top features): cp, ca, oldpeak, exang, age

Logistic Regression coefficients → indicate direction of impact on disease risk.

Decision Tree importance → indicates how much a feature influences tree splits.

ROC Curve

ROC (Receiver Operating Characteristic) plots True Positive Rate vs False Positive Rate at different thresholds.

AUC (Area Under Curve) shows overall model performance (closer to 1 = better).

Useful for medical datasets with class imbalance.

Exploratory Data Analysis (EDA)

Target distribution shows balance between disease and no disease.

Correlation heatmap helps identify influential features.

Strongest predictors: cp, oldpeak, ca, exang.
