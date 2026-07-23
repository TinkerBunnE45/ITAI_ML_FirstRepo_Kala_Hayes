# ITAI-1371: Intro to Machine Learning

> **Lab 07: Lab 07 Model evaluation**
> **Class:** 6263-ITAI-1371-S10-12321
> **Group:** Group 3

## 👥 Team Members
* **Kala Hayes**
* **Edwin Alvarado**
* **Anashrah Adil**
* **Zain Ahmed**

# Titanic Survival Prediction & Model Evaluation

A machine learning project that predicts passenger survival outcomes from the Titanic disaster using Logistic Regression. This project focuses on implementing advanced model evaluation techniques, including confusion matrices, precision/recall metrics, and cross-validation, to move beyond simple accuracy.

## 📊 Project Overview

This repository demonstrates a complete machine learning workflow:
1. **Data Cleaning & Preprocessing:** Handling missing data values and encoding categorical text features into numerical variables.
2. **Model Training:** Implementing a Logistic Regression classifier using `scikit-learn`.
3. **Advanced Evaluation:** Breaking down model errors to understand its strengths, weaknesses, and performance stability.

## 🗃️ Dataset

The model utilizes the classic **Titanic Dataset** fetched directly from the Data Science Dojo repository:
* **Features Used:** `Age`, `Pclass` (Passenger Class), `Sex`, and `Fare`.
* **Target Variable:** `Survived` (0 = Died, 1 = Survived).

---

## 📈 Model Performance & Evaluation

### 1. Confusion Matrix
The model was tested on an unseen 20% validation split (179 total passengers). 

* **True Negatives (Died):** 90
* **True Positives (Survived):** 54
* **False Positives:** 15 (Predicted survival, but the passenger died)
* **False Negatives:** 20 (Predicted death, but the passenger survived)

### 2. Classification Report
Breaking down performance across both classes using Precision, Recall, and F1-Score:

```text
              precision    recall  f1-score   support

        Died       0.82      0.86      0.84       105
    Survived       0.78      0.73      0.76        74

    accuracy                           0.80       179
```

* **Precision (Survived = 78%):** When the model predicts a passenger survived, it is correct 78% of the time.
* **Recall (Survived = 73%):** The model successfully identifies 73% of all actual survivors in the test data.

### 3. K-Fold Cross-Validation
To guarantee that the model's performance isn't a result of a "lucky" data split, a **5-Fold Cross-Validation** was performed across the entire dataset.

* **Average CV Score:** `78.68%`
* **Standard Deviation:** `0.0094` (Less than 1% variance, indicating high model stability)

---

## 🛠️ Requirements & Installation

To run this notebook locally, ensure you have Python installed along with the following libraries:

```bash
pip install pandas scikit-learn seaborn matplotlib
```

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com
   ```
2. Open the `.ipynb` notebook file using Google Colab, Jupyter Notebook, or VS Code.
3. Run the cells sequentially to preprocess the data, train the model, and render the evaluation metrics.

---

## 💡 Key Takeaways & Trade-offs
* **Precision vs. Recall:** Depending on real-world constraints, optimization metrics must change. In high-stakes environments like credit card fraud, maximizing *Precision* protects customer friction. In scenarios like predictive machinery maintenance, maximizing *Recall* is vital to prevent catastrophic failures.
* **The Power of Cross-Validation:** While our initial single train-test split yielded an optimistic accuracy of `80.00%`, 5-fold cross-validation revealed a more accurate, generalized baseline performance of `78.68%`.

