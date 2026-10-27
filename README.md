# ai-club
Interpretable machine learning for diabetes risk prediction using Logistic Regression and SHAP on the Pima Indians Diabetes Dataset.

# Interpretable Machine Learning for Diabetes Risk Prediction

## Project Overview

This project investigates the behavior and interpretability of a Logistic Regression classifier trained on the Pima Indians Diabetes Dataset.

The dataset contains 768 patient records and eight input features: pregnancies, glucose, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, and age. The target variable indicates the recorded diabetes outcome.

The project uses data visualization to investigate how the model behaves, which input patterns are associated with correct and incorrect predictions, and how the model's learned relationships can be interpreted.

## Model and Dataset

- **Model:** Logistic Regression
- **Dataset:** Pima Indians Diabetes Dataset
- **Explainability technique:** SHAP
- **Dataset sources:**
  - [Kaggle](https://www.kaggle.com/code/mragpavank/pima-indians-diabetes-database)
  - [OpenML](https://www.openml.org/d/37)
  - [Github](https://github.com/ragav0705/diabetes-risk-prediction-case-study)
  - [XAI_Diabetes](https://github.com/Atharva309/XAI_diabetes)

## Phase I: How Does the Model Behave?

We will analyze model predictions using visualizations of prediction outcomes, feature distributions, and error patterns. We will investigate differences between correctly and incorrectly classified records rather than relying only on aggregate performance metrics.

## Phase II: What Did the Model Learn?

We will investigate the model's learned feature relationships using SHAP explanations and at least one additional analysis technique. We will compare the insights from these techniques to understand the model's behavior observed in Phase I.
