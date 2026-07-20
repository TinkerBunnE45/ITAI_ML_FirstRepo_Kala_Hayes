# ITAI-1371: Intro to Machine Learning

> **Lab 05: Data Preprocessing and Feature Engineering**
> **Class:** 6263-ITAI-1371-S10-12321
> **Group:** Group 3
> 
## 👥 Team Members
* **Kala Hayes**
* **Edwin Alvarado**
* **Anashrah Adil**
* **Zain Ahmed**

# Titanic Passenger Analysis: Linear and Logistic Regression

This repository contains a hands-on data science lab focusing on **Supervised Machine Learning** using the classic Titanic dataset. The goal of this project is to clean passenger data and apply two distinct machine learning models to solve both regression and classification problems using Python's `scikit-learn` library.

## 📋 Project Objectives
* **Data Preprocessing:** Handle missing data (`NaN` values) and encode categorical variables into numerical values.
* **Regression Analysis:** Build a Linear Regression model to predict a continuous numerical value (ticket fare).
* **Classification Analysis:** Build a Logistic Regression model to predict a discrete binary outcome (passenger survival).
* **Model Evaluation:** Evaluate model performance using appropriate data science metrics.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Environment:** Jupyter Notebook / Google Colab
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (`LinearRegression`, `LogisticRegression`, `train_test_split`, `mean_squared_error`, `accuracy_score`)

---

## 🚀 Lab Workflow & Implementation

### 1. Data Cleaning & Preprocessing
* Converted the categorical text column `Sex` into numerical values (`'male': 0`, `'female': 1`) so it could be processed by the classification algorithm.
* Addressed missing values (`NaN`) in the `Age` column using a foolproof imputation method (`.fillna()`), preventing runtime crashes during model execution.

### 2. Task 1: Linear Regression (Fare Prediction)
* **Problem:** Predict the continuous numerical dollar amount of a passenger's ticket `Fare` based on features like `Age` and `Pclass`.
* **Evaluation Metric:** Evaluated using **Mean Squared Error (MSE)** and its square root (RMSE) to determine the average mathematical distance between the predicted prices and actual historical ticket costs.

### 3. Task 2: Logistic Regression (Survival Prediction)
* **Problem:** Predict whether a passenger `Survived` (1) or did not survive (0) based on their `Age`, `Pclass`, and `Sex`.
* **Evaluation Metric:** Evaluated using **Accuracy Score** to calculate the exact percentage of correct binary category predictions on the unseen testing dataset.

---

## 📝 Key Concepts Learned
* **Data Quality Matters:** Machine learning algorithms cannot natively compute equations with missing values (`NaN`). Data imputation is a mandatory step in the machine learning workflow.
* **Regression vs. Classification:** 
  * *Regression* deals with continuous scales where errors are measured by distance (e.g., how many dollars off).
  * *Classification* deals with exact categorical labels where success is binary (e.g., right or wrong guessing).
* **Metric Application:** Why `accuracy_score` is ideal for categorization but completely useless for measuring precise continuous metrics like pricing, which require `mean_squared_error`.
