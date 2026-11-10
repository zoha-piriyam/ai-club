# AI Club Group
Interpretable machine learning for diabetes risk prediction using Logistic Regression and SHAP on the Pima Indians Diabetes Dataset.

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
## Team and Pairs

| Human-only pair (Group A) | AI-aided pair (Group B) |
|---|---|
| Zahra Piriyam, Rawan Arafa | Syeda Nusraht Khaledur, Selvasubramanian Sivagirinathan |

## Repository Structure

| File | Description |
|---|---|
| `data-preprocessing.ipynb` | Loads the dataset, creates a stratified 80/20 train/test split (`random_state=42`) and saves the split files |
| `X_train.xls`, `X_test.xls`, `y_train.xls`, `y_test.xls` | Train/test split (CSV content) |
| `model-training.ipynb` | Trains Logistic Regression (C=1.0, solver=lbfgs, max_iter=1000, random_state=42), evaluates it on the test set and saves the predictions |
| `logistic_regression_model.joblib`, `imputer.joblib`, `scaler.joblib` | Saved model, imputer and scaler |
| `prediction_results.csv` | 154 test records: input features, actual outcome, predicted label, probability |
| `phase1-human group.ipynb` | Phase I analysis – human-only pair (Group A) |
| `phase1-ai-group.ipynb` | Phase I analysis – AI-aided pair (Group B) |
| `ai-interactions/phase1_ai_record.md` | GenAI interaction record (Phase I) |
| `ai_reflection_midpoint.md` | Midpoint reflection on GenAI usage |
| `team-info.json`, `workload.json` | Team members and workload |

## How to Run

Required packages: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` (version 1.7.2 to load the saved model).

Open and run either Phase I notebook:
- `phase1-human group.ipynb`
- `phase1-ai-group.ipynb`

Both notebooks only use `prediction_results.csv`, which is included in the repository.

## Phase II: What Did the Model Learn?

We will investigate the model's learned feature relationships using SHAP explanations and at least one additional analysis technique. We will compare the insights from these techniques to understand the model's behavior observed in Phase I.
