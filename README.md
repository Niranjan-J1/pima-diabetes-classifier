# PIMA Diabetes Classification

This is an **older machine learning project** focused on binary classification of diabetes based on the PIMA Indian dataset. The project demonstrates data preprocessing, feature engineering, model training, evaluation, and visualization. 

> ⚠️ Note: This project was developed as an early portfolio project. The frontend is not included, as it was lost at the time this repo was made .

---

## Dataset

The dataset used is publicly available from Kaggle: [Diabetes Dataset](https://www.kaggle.com/datasets/mathchi/diabetes-data-set).  
It contains 768 entries with the following features:

- Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age
- Target: Outcome (0 = Healthy, 1 = Diabetic)

---

## Features & Preprocessing

- Handled missing values (replaced 0s with median values per Outcome group)
- Created **engineered features** to improve model performance, including:
  - `N0 = BMI * SkinThickness`
  - `N8 = Pregnancies / Age`
  - `N14 = Age / Insulin`
  - Several binary flags based on feature thresholds
- Scaled numerical features and applied one-hot encoding to categorical variables
- Label encoded binary variables

---

## Models Used

1. **LightGBM Classifier** (optimized with RandomizedSearchCV)
2. **K-Nearest Neighbors (KNN)**
3. **Voting Classifier** combining LightGBM and KNN

### Model Evaluation

- 5-fold cross-validation used for robust evaluation
- Metrics reported:
  - Accuracy, Precision, Recall, F1-score, ROC-AUC
- Confusion matrices, ROC curves, and precision-recall curves were generated using Plotly

## Visualizations

The project includes interactive and static visualizations for:

- Outcome distributions (bar charts, pie charts)
- Feature distributions and correlations
- Custom feature vs target analysis
- Confusion matrices, ROC curves, precision-recall curves

Tools used:

- Matplotlib, Seaborn, Plotly, Yellowbrick

---

