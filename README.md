# Predicting Employee Attrition Using Machine Learning

## Table of Contents
- [Project Setup](#project-setup)
- [Project Introduction](#project-introduction)
- [Data](#data)
- [Approach](#approach)
- [Model Comparison & Results](#model-comparison--results)
- [Key Insights](#key-insights)
- [Conclusions](#conclusions)

---

## Project Setup

To set up this project environment locally:

### Option 1: Using Conda
1. Ensure [Anaconda](https://www.anaconda.com/) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) is installed.
2. Navigate to the project root directory.
3. Run:
   ```bash
   conda env create -f environment.yml
   conda activate attrition-project
   ```

### Option 2: Using Pip
1. (Optional) Create a virtual environment.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Project Introduction

Employee attrition — when employees voluntarily leave an organization — poses significant financial and operational challenges. This project applies statistical analysis and supervised machine learning to identify the key drivers of attrition and build predictive models to forecast which employees are at risk.

The goal is to empower HR teams with insights and tools to proactively improve employee retention and workplace satisfaction.

---

## Data

The dataset is the **IBM HR Analytics Employee Attrition & Performance** dataset from Kaggle:  
🔗 [Kaggle Dataset Link](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

It contains 1,470 fictional employee records with features such as:

- **Demographics:** Age, Gender, Marital Status  
- **Job Info:** Job Role, Department, Years at Company, OverTime  
- **Satisfaction Metrics:** JobSatisfaction, EnvironmentSatisfaction, WorkLifeBalance  
- **Compensation & Performance:** MonthlyIncome, StockOptionLevel, PerformanceRating  
- **Target Variable:** `Attrition` (Yes/No)

---

## Approach

The project followed a comprehensive data science pipeline:

1. **Data Cleaning & Feature Engineering**
   - Converted time-based columns and encoded categorical variables
   - Addressed multicollinearity and missing values

2. **Exploratory Data Analysis (EDA)**
   - Uncovered patterns and correlations between features and attrition
   - Highlighted high-risk groups by satisfaction level, job role, and workload

3. **Statistical Testing**
   - Performed t-tests and chi-square tests to determine significant feature differences
   - Built logistic regression models for statistical inference

4. **Modeling & Evaluation**
   - Trained and compared **Logistic Regression**, **Random Forest**, and **AdaBoost** models
   - Applied **SMOTE** for class balancing and performed **hyperparameter tuning**
   - Used multiple metrics: accuracy, precision, recall, F1, and ROC AUC

5. **Interpretability**
   - Analyzed feature importances via model coefficients, permutation importance, and SHAP values

---

## Model Comparison & Results

| Model               | Configuration                   | Accuracy | Precision | Recall | F1 Score | ROC AUC Score |
|---------------------|----------------------------------|----------|-----------|--------|----------|----------------|
| Logistic Regression | Tuned on Original Data           | **0.874** | 0.708     | 0.362  | **0.479** | **0.824**      |
| Random Forest       | SMOTE (Default)                  | 0.823    | 0.391     | 0.191  | 0.257    | 0.702          |
| AdaBoost            | SMOTE (Default)                  | 0.799    | 0.400     | **0.511** | 0.449    | 0.735          |

✅ **Selected Model:** Logistic Regression (Tuned on Original Data)  
This model offered the best balance of recall, precision, and interpretability.

---

## Key Insights

- **Workload and dissatisfaction** are the leading drivers of attrition:
  - Employees with **OverTime**, **low job satisfaction**, and **poor work-life balance** were most likely to leave.
- **Early tenure and job role** are key risk indicators:
  - **Sales Representatives** and **Lab Technicians** showed high turnover rates.
  - Attrition peaked within the first 2–3 years of employment.
- **Personal context matters**:
  - **Single** employees and those with longer **commutes** had higher attrition.
- **Satisfaction scores, engagement levels, and promotion delays** all play a role in employee retention.

---

## Conclusions

This analysis confirms that employee attrition is a **multifaceted issue** influenced by satisfaction, engagement, role expectations, and work-life factors.

Our best-performing model — **Logistic Regression with tuning** — not only achieved strong predictive performance but also provided clear and interpretable insights into what drives turnover.

These results can help organizations:
- **Proactively identify at-risk employees**
- **Design data-informed HR interventions**
- **Improve employee experience and retention**

By applying statistical rigor and machine learning, this project offers a blueprint for tackling attrition using real-world data and practical, actionable insights.
