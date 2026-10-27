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
- **Task:** Binary classification
- **Explainability technique:** SHAP
- **Dataset sources:**
  - [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)
  - [OpenML](https://www.openml.org/d/37)

## Research Questions

1. How does Logistic Regression behave across different patient groups, and what patterns are associated with incorrect predictions?
2. Which clinical features contribute most to the model's predictions, and how do their contributions differ between correct and incorrect predictions?
3. How can SHAP visualizations help explain individual predictions and overall model behavior?

## Phase I: How Does the Model Behave?

We will analyze model predictions using visualizations of prediction outcomes, feature distributions, and error patterns. We will investigate differences between correctly and incorrectly classified records rather than relying only on aggregate performance metrics.

## Phase II: What Did the Model Learn?

We will investigate the model's learned feature relationships using SHAP explanations and at least one additional analysis technique. We will compare the insights from these techniques to understand the model's behavior observed in Phase I.

## AI4Vis Comparison

Two pairs will investigate the same model and task, switching between AI-assisted and human-only workflows across the two phases. We will compare their visualization choices, findings, analysis depth, and the limitations of AI assistance.

## Limitations

The dataset represents a specific population and should not be assumed to represent all populations. Model predictions and SHAP explanations do not establish causation and must not be interpreted as medical diagnoses.

## Technologies

- Python
- pandas and NumPy
- scikit-learn
- SHAP
- Matplotlib and Seaborn
- Jupyter Notebook

## Team

Team name: TODO

Group members: TODO

