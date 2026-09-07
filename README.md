# Evaluating Bias and Fairness in Machine Learning Models for Diabetes Prediction

## Overview

Machine learning is increasingly being used in healthcare to support disease prediction and clinical decision-making. However, achieving high predictive accuracy does not necessarily mean that a model performs equally across different demographic groups.

This project evaluates the **performance, bias, and fairness of supervised machine learning models for diabetes prediction**. Three classification algorithms — **Logistic Regression, Decision Tree, and Random Forest** — are developed and compared using an anonymized diabetes prediction dataset containing approximately 100,000 patient records.

In addition to evaluating traditional predictive performance, the project investigates whether the models produce different outcomes across **gender and age groups**. Fairness metrics are used alongside standard classification metrics to provide a more comprehensive assessment of model behavior.

---

## Research Aim

The aim of this project is to evaluate bias and fairness in machine learning models used for diabetes prediction and to compare the performance and fairness of different supervised learning algorithms.

## Objectives

The main objectives are:

- To compare bias in diabetes prediction models.
- To compare fairness between supervised learning algorithms.
- To assess model fairness using selected fairness metrics.
- To evaluate model performance across demographic groups.

---

## Dataset

The project uses the **Diabetes Prediction Dataset** obtained from Kaggle.

The dataset contains approximately **100,000 anonymized patient records** with healthcare and demographic attributes such as:

- Gender
- Age
- Hypertension
- Heart disease
- Smoking history
- Body Mass Index (BMI)
- HbA1c level
- Blood glucose level
- Diabetes outcome

After data cleaning and preprocessing, the dataset is prepared for machine learning model development and demographic fairness analysis.

---

## Machine Learning Models

Three supervised machine learning algorithms are evaluated in this project:

### 1. Logistic Regression

Logistic Regression is used as an interpretable linear baseline for estimating the probability of diabetes based on patient characteristics.

### 2. Decision Tree

Decision Tree classification uses hierarchical decision rules to capture nonlinear relationships between clinical variables and diabetes outcomes.

### 3. Random Forest

Random Forest combines multiple decision trees using ensemble learning to improve predictive stability and overall classification performance.

---

## Data Preprocessing

The preprocessing pipeline includes:

- Data inspection and cleaning
- Removal of unsuitable demographic records
- Encoding of categorical variables
- Feature scaling using `StandardScaler`
- Creation of demographic groups for fairness evaluation
- Stratified train-test splitting
- 80% training and 20% testing data

The demographic fairness analysis focuses primarily on **gender and age groups**.

---

## Model Evaluation

The predictive performance of each model is evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

These metrics provide a comparison of how effectively each machine learning algorithm predicts diabetes.

---

## Fairness Evaluation

Model accuracy alone cannot determine whether predictions are fair across different patient populations. Therefore, fairness analysis is performed across demographic subgroups.

The project evaluates fairness using:

- **Demographic Parity Difference**
- **Equalized Odds Difference**
- **Per-group Accuracy**
- **Gender-based Comparison**
- **Age-group Comparison**

The **Fairlearn** Python library is used to support the demographic fairness evaluation.

---

## Technologies and Libraries

The project is implemented in **Python** using a Jupyter/Google Colab environment.

Major technologies and libraries include:

- Python
- Pandas
- NumPy
- Scikit-learn
- Fairlearn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

---

## Project Workflow

1. Load the diabetes prediction dataset
2. Inspect and clean the data
3. Perform exploratory and descriptive analysis
4. Encode categorical variables
5. Standardize numerical features
6. Create demographic groups
7. Split the dataset into training and testing sets
8. Train Logistic Regression
9. Train Decision Tree
10. Train Random Forest
11. Evaluate classification performance
12. Generate confusion matrices
13. Evaluate fairness across gender groups
14. Evaluate fairness across age groups
15. Compare per-group accuracy
16. Analyze feature importance
17. Compare overall model performance and fairness

---

## Key Findings

The experimental results show that all three machine learning models achieve **more than 96% overall accuracy** in diabetes prediction.

However, high overall accuracy does not automatically guarantee equal performance across demographic groups. The fairness analysis identifies more meaningful differences across **age groups** than across gender groups.

Among the three evaluated algorithms, **Random Forest demonstrates the strongest overall predictive performance while maintaining a comparatively balanced fairness profile across the evaluated demographic groups**.

These findings highlight the importance of evaluating both **predictive performance and algorithmic fairness** when machine learning systems are considered for healthcare applications.

---

## Conclusion

This project demonstrates that evaluating healthcare machine learning models should extend beyond traditional accuracy metrics.

By comparing Logistic Regression, Decision Tree, and Random Forest using both predictive performance and demographic fairness measures, the study provides a broader understanding of how different algorithms behave across patient groups.

The results emphasize the importance of **fairness-aware and responsible machine learning practices in healthcare**, particularly when predictive systems may contribute to decisions affecting different demographic populations.

---

## Repository Structure

```text
├── Code.ipynb
├── README.md
└── document.docx
