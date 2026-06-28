# ITAI-1371: Intro to Machine Learning

> **Lab 05: Data Preprocessing and Feature Engineering**
> **Class:** 6263-ITAI-1371-S10-12321
> **Group:** Group 3

## 👥 Team Members
* **Kala Hayes**
* **Edwin Alvarado**
* **Anashrah Adil**
* **Zain Ahmed**

## 📌 Project Overview
This project uses **Google Colab** to execute critical data preprocessing and feature engineering steps on the Titanic passenger dataset for Lab 05. Moving past initial visual exploration, our group focused on structural data refinement: handling missing values, converting text categories into machine-readable mathematical formats, and standardizing feature scales. These steps ensure that subsequent machine learning models train efficiently without scale or formatting bias.

## 🚀 Run this Project in Google Colab
You can run this notebook entirely in your browser without installing anything locally. Click the badge below to open it directly in Google Colab:

[![Open In Colab](https://google.com)](https://google.com)

## 📂 File Structure

| File | Description |
| :--- | :--- |
| `Module_05_Lab_Exercise.ipynb` | Google Colab notebook containing preprocessing Python code and outputs. |
| `Lab 05.pdf` | Lab instructions and data engineering reference material. |
| `README.md` | Comprehensive overview and progress tracking. |

## 🛠️ Tech Stack & Libraries
We utilized the standard Python data science stack within a Google Colab Hosted Runtime:
* **Python 3:** Base programming language.
* **Pandas:** For handling dataframes, managing missing values, and hot-encoding categorical matrices.
* **Scikit-Learn (preprocessing):** Specifically leveraging `StandardScaler` to perform Z-score standardization.

## 📊 Key Findings & Pipeline Steps
* **Statistical Imputation:** Diagnosed 177 missing entries in the `Age` feature and resolved them using robust median imputation to protect against distributional distortion caused by outliers.
* **Categorical Matrix Transformation:** Transformed text columns (`Sex`, `Embarked`) into binary flags via `pd.get_dummies()`. Applied `drop_first=True` to structurally eliminate the dummy variable trap (multicollinearity).
* **Feature Scale Stabilization:** Identified extreme scale variance between `Age` (0-80) and `Fare` (0-512). Applied a `StandardScaler` transformation to achieve a mean of 0 and standard deviation of 1, preventing the higher-magnitude `Fare` metric from overwhelming model weight allocation.
* **Pipeline Sequencing:** Verified that preprocessing steps are strictly linear. Scaling algorithms will throw runtime exceptions if numerical columns still contain empty `NaN` fragments.

## 🚀 How to Run
1. Open [Google Colab](https://google.com).
2. Upload the `Module_05_Lab_Exercise.ipynb` file from this repository.
3. Execute the cells sequentially to watch the raw Titanic dataset become fully optimized for machine learning algorithms.

