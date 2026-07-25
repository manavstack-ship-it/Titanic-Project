# Titanic-Project
# 🚢 Titanic - Machine Learning from Disaster

An exploratory data analysis (EDA) and binary classification project built on the famous Kaggle Titanic dataset. This project analyzes passenger demographics, ticket information, and cabin locations to build predictive models for passenger survival.

---

## 📌 Project Overview
On April 15, 1912, the RMS Titanic sank after colliding with an iceberg, resulting in the loss of 1,502 lives out of 2,224 passengers and crew. While survival involved an element of luck, certain groups—such as women, children, and upper-class passengers—were more likely to survive than others.

The goal of this project is to:
1. Conduct Exploratory Data Analysis (EDA) to discover key patterns in passenger survival.
2. Preprocess and clean real-world tabular data (imputing missing values, feature engineering, and encoding).
3. Train and compare Machine Learning classifiers to predict whether a passenger survived (`1`) or died (`0`).

---

## 📊 Dataset Description
The dataset contains information on individual passengers aboard the Titanic.

| Feature | Definition | Key / Notes |
| :--- | :--- | :--- |
| `PassengerId` | Unique ID per passenger | Numeric ID |
| `Survived` | Survival target variable | `0` = No, `1` = Yes |
| `Pclass` | Ticket class | `1` = 1st (Upper), `2` = 2nd (Middle), `3` = 3rd (Lower) |
| `Name` | Passenger full name | Text |
| `Sex` | Gender | `male`, `female` |
| `Age` | Age in years | Continuous (contains missing values) |
| `SibSp` | # of siblings / spouses aboard | Integer |
| `Parch` | # of parents / children aboard | Integer |
| `Ticket` | Ticket number | String |
| `Fare` | Passenger fare paid | Continuous |
| `Cabin` | Cabin number | String (high percentage of missing values) |
| `Embarked` | Port of Embarkation | `C` = Cherbourg, `Q` = Queenstown, `S` = Southampton |

---

## 🛠️ Tech Stack & Dependencies
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (Logistic Regression, Random Forest, XGBoost)

---

## ⚙️ Workflow & Key Insights
1. **Data Cleaning & Imputation:** Imputed missing values for `Age` (median by class/title) and `Embarked` (mode). Dropped/transformed highly missing columns like `Cabin`.
2. **Feature Engineering:** Extracted passenger titles (`Mr`, `Mrs`, `Miss`, etc.) from names and engineered family size (`FamilySize = SibSp + Parch + 1`).
3. **Model Training:** Evaluated baseline models (Logistic Regression, Decision Trees) against ensemble methods (Random Forest, Gradient Boosting).

