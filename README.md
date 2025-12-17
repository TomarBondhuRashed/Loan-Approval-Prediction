# 🏦 Loan Eligibility Prediction: Banking Classification

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project automates the loan eligibility process (real-time) based on customer details provided while filling out online application forms. The goal is to predict whether a loan should be **Approved** or **Rejected** based on parameters like Gender, Marital Status, Education, Income, and Credit History.

This project focuses on **handling categorical data** and **visualizing decision logic** using Decision Trees.

---

## 🧹 Data Preprocessing Strategy
Banking data contains mixed types (Numbers + Text).
* **Handling Categorical Data:** Used `LabelEncoder` to convert features like `Education` ("Graduate") and `Property_Area` ("Urban") into machine-readable numbers.
* **The "Dependents" Issue:** The raw dataset contained values like `3+`, which I programmatically cleaned to `4` to allow numerical analysis.
* **Missing Values:** Imputed numerical columns with Median and categorical columns with Mode (most frequent).

---

## 📊 Key Insights (EDA)
Exploratory Data Analysis revealed the single most critical factor for approval:

* **Credit History:** Applicants with a Credit History of `1.0` (Good) were overwhelmingly approved. Those with `0.0` (Bad) were almost universally rejected, regardless of their income.

*(Note: Upload your Bar Chart here)*
![Credit History Plot](images/credit_history_plot.png)

---

## 🤖 Model Performance
I compared **Logistic Regression** (Standard Banking Model) vs. **Decision Trees** (Explainable AI).

* **Accuracy:** ~80%
* **Model Explainability:** The Decision Tree visualization confirmed that the "Root Node" (the first decision the model makes) is strictly based on Credit History.

*(Note: Upload your Decision Tree image here)*
![Decision Tree Logic](images/decision_tree.png)

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/loan-prediction.git](https://github.com/your-username/loan-prediction.git)
