# Heart Disease Prediction Using Machine Learning

## Overview

This project uses machine learning classification algorithms to predict the presence of heart disease based on patient health-related attributes.

The project demonstrates data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction using Python and Scikit-learn.

## Objectives

- Analyze heart disease data using Exploratory Data Analysis.
- Clean and preprocess the dataset.
- Train and compare machine learning classification models.
- Evaluate models using multiple performance metrics.
- Save and reuse the best-performing model.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Dataset

- Original records: 1,025
- Records after duplicate removal: 302
- Features: 13
- Target variable: 1

The target variable represents:
- `0` – No Heart Disease
- `1` – Heart Disease

## Exploratory Data Analysis

The following visualizations were performed:

- Heart disease distribution
- Age distribution
- Age vs heart disease
- Cholesterol distribution
- Cholesterol vs heart disease
- Maximum heart rate distribution
- Maximum heart rate vs heart disease
- Correlation heatmap

## Machine Learning Models

Two classification algorithms were implemented:

1. Logistic Regression
2. Gaussian Naive Bayes

A preprocessing pipeline was created using:
- StandardScaler for numerical features.
- OneHotEncoder for categorical features.
- ColumnTransformer to combine preprocessing steps.
- Scikit-learn Pipeline for model training and prediction.

## Model Evaluation

| Metric | Logistic Regression | Gaussian Naive Bayes |
|---|---:|---:|
| Accuracy | 83.61% | 80.33% |
| Precision | 84.85% | 81.82% |
| Recall | 84.85% | 81.82% |
| F1-score | 84.85% | 81.82% |
| ROC-AUC | 90.48% | 89.39% |

### Cross-validation

Training-set 5-fold cross-validation:

| Model | Mean Accuracy |
|---|---:|
| Logistic Regression | 83.39% |
| Gaussian Naive Bayes | 80.52% |

Logistic Regression was selected as the final model based on its performance in the evaluated results.

## Model Saving

The trained Logistic Regression pipeline was saved using Joblib:

`heart_disease_model.pkl`

The saved model was successfully loaded and used to generate predictions for sample patient records.

## Project Structure

```text
Heart_Disease_Prediction/
│
├── heart.csv
├── Heart_Disease_Prediction.ipynb
├── heart_disease_model.pkl
└── README.md
```

## How to Run

1. Clone the repository.
2. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `Heart_Disease_Prediction.ipynb`.
5. Run the notebook cells sequentially.

## Conclusion

Logistic Regression achieved an accuracy of 83.61% and ROC-AUC of 90.48% on the test dataset. The project demonstrates a complete machine learning workflow, from data cleaning and visualization to model evaluation and saving a reusable prediction pipeline.

## Disclaimer

This project is intended for educational purposes only. It is not a clinically validated medical diagnostic tool and should not be used for medical decisions.