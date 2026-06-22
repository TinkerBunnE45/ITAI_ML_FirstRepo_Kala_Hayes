
#Lab 04: Data Exploration and Visualization**
> **Class:** 6263-ITAI-1371-S10-12321
> **Group:** Team ML_1371_12321

## 👥 Team Members Group 3
* **Edwin Alvarado**
* **Kala Hayes**
* **Anashrah Adil**
* **Zain Ahmed**

## 📌 Project Overview
This project uses **Google Colab** to perform Exploratory Data Analysis (EDA) on the Titanic passenger dataset for Lab 04. The analysis investigates how factors like socio-economic class, gender, and age heavily influenced a passenger's chance of survival. Our group shifted focus from purely algorithms to the critical stages of loading, exploring, and visualizing data to ensure model accuracy and balance.



## 📂 File Structure

| File | Description |
| :--- | :--- |
| `Module_04_Lab_Exercise.ipynb` | Google Colab notebook containing Python code and outputs. |
| `Lab 04.pdf` | Lab instructions and reference material. |
| `README.md` | Comprehensive overview, knowledge check answers, and progress. |

## 🛠️ Tech Stack & Libraries
We utilized the standard Python data science stack within a Google Colab Hosted Runtime:
* **Python 3:** Base programming language.
* **Pandas:** For loading datasets, data cleaning, and structured DataFrames.
* **Matplotlib:** For rendering foundational graphs and survival trends.
* **Seaborn:** For advanced statistical visualizations to slice multi-categorical data.

## 📊 Key Findings
* **Baseline Metrics:** Functions like `.describe()` and `.info()` revealed an average passenger age of 29, a baseline survival rate of roughly 38%, and critical missing values in the `Age` and `Cabin` columns.
* **Socio-Economic & Gender Bias:** Categorical count plots utilizing the `hue` parameter confirmed a stark survival advantage for first-class passengers and female travelers.
* **Age Distribution:** Integrated Seaborn `FacetGrid` histograms illustrated that children had high survival rates, whereas adult males faced the lowest mathematical probability of survival.
* **Economic Advantage:** A detailed violin plot comparing `Fare` to `Survived` clearly demonstrated that individuals who purchased high-tariff tickets had a vastly increased likelihood of rescuing.
