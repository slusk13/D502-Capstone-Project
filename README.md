# Predicting Employee Attrition Using Machine Learning

## Table of Contents
- [Project Setup](#project-setup)
- [Project Introduction](#project-introduction)
- [Data](#data)
- [Project Outcomes/Model Metrics](#project-outcomesmodel-metrics)
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

### Option 2: Using Pip
1. (Optional) Create a virtual environment.
2. Install dependencies:
```bash
pip install -r requirements.txt
```
---

## Project Introduction
Employee attrition is a critical concern for organizations due to its financial and operational implications. This project leverages data analytics and machine learning to identify key factors contributing to employee turnover and builds a predictive model to forecast attrition. The goal is to support HR professionals with actionable insights and tools for proactive retention strategies.

---

## Data
The dataset used is the IBM HR Analytics Employee Attrition & Performance dataset, available on Kaggle:
🔗 [Kaggle Dataset Link](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

This fictional dataset contains information on 1,470 employees, including demographic details, job satisfaction, compensation, performance metrics, and attrition status. Each row represents an individual employee, and the dataset includes both categorical and numerical features relevant to predicting attrition.

Key variables include:

- `Attrition` (target variable: Yes/No)

- `JobSatisfaction`, `WorkLifeBalance`, `OverTime`

- `MonthlyIncome`, `YearsAtCompany`, `JobRole`, and more

No restricted or proprietary information is used in this project.

---

## Project Outcomes/Model Metrics

---

## Conclusions