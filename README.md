Heart Disease Prediction – By Samiha Azeem
Objective
We want to guess if someone might have heart disease using information about their health, like age, blood pressure, and heart rate. The idea is to make a simple and smart tool that helps predict the risk.

About the Data

The dataset has 13 health features and 1 target:

age – How old the person is
sex – 1 = male, 0 = female
cp – Type of chest pain (0–3)
trestbps – Blood pressure at rest
chol – Cholesterol level
fbs – Fasting blood sugar > 120 (1 = yes, 0 = no)
restecg – Resting ECG result (0–2)
thalach – Maximum heart rate achieved
exang – Exercise induced angina (1 = yes, 0 = no)
oldpeak – ST depression after exercise
slope – Slope of ST segment (0–2)
ca – Number of major blood vessels
thal – Thalassemia type (1,2,3)

Target:

target – 1 = has heart disease, 0 = does not have heart disease

How We Did It

Look at the data
Checked for missing values (there were none)
Made plots to see patterns
Split into training (80%) and testing (20%)
Scaled numbers for Logistic Regression

Models Used

Logistic Regression: gives a probability of having heart disease
Decision Tree: decides step by step which features are most important

Check performance

Accuracy – How often the model is correct
Confusion Matrix – Shows correct vs wrong predictions
ROC Curve – Shows how well the model separates sick and healthy people
Feature Importance – Which features matter most

Results
Model	Accuracy	ROC-AUC
Logistic Regression	0.85	0.91
Decision Tree	0.85	0.88

Observations:

Both models are correct about 85% of the time
Logistic Regression shows how each feature affects risk
Decision Tree shows which features are most important for decision-making
Most important features: chest pain (cp), ST depression (oldpeak), number of vessels (ca)

Feature Importance

Logistic Regression: cp, slope, thalach – shows which features increase or decrease risk
Decision Tree: cp, ca, oldpeak, exang, age – shows which features the tree uses to make decisions

ROC Curve

ROC shows how well the model separates sick and healthy people
AUC (area under curve) closer to 1 → better model

Exploratory Data Analysis (EDA)

We checked the data with charts
Target is pretty balanced
Most important features: cp, oldpeak, ca, exang
