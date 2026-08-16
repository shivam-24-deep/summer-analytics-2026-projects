
# Week 2 Hackathon — Customer Conversion Prediction

## 📌 Overview

This project was developed as part of the **Week 2 Hackathon** during Summer Analytics 2026.

The objective was to build a Machine Learning model to predict whether a user would **convert** based on demographic, behavioral, browsing, and campaign-related information.

## 📊 Dataset

The notebook works with:

* **Training data:** 10,000 records
* **Public test data:** 3,000 records
* **Private test data:** 3,000 records
* **Features:** 13 predictive/input columns
* **Target:** `Converted`

The target distribution in the training dataset was:

* `0`: 69.13%
* `1`: 30.87%

## 🔍 Exploratory Data Analysis

The project includes analysis of:

* Dataset structure and data types
* Missing values
* Target-class distribution
* Numerical feature distributions
* Age and income relationships with conversion
* Correlation between numerical variables

## 🧹 Data Preprocessing

The workflow included:

* Median imputation for missing `Age`
* Median imputation for missing `Income`
* Median imputation for missing `Time_On_Site`
* Categorical feature encoding using `LabelEncoder`

## ⚙️ Feature Engineering

Additional features were created:

### Engagement

```text
Pages_Viewed + Products_Viewed
```

### Purchase Ratio

```text
Previous_Purchases / (Pages_Viewed + 1)
```

### Income Per Page

```text
Income / (Pages_Viewed + 1)
```

These features were added to capture additional behavioral information from the available data.

## 🤖 Models Explored

### Random Forest

A Random Forest classifier with:

* 500 estimators
* Balanced class weights
* Random state: 42

Recorded validation F1:

**0.3326**

### CatBoost

A CatBoost classifier was then explored with:

* 500 iterations
* Depth: 6
* Learning rate: 0.05
* Logloss objective
* F1 evaluation metric

Recorded validation F1:

**0.3828**

The notebook also includes GPU-based CatBoost training using a **Tesla T4 GPU** in Google Colab.

## 📈 Evaluation

The models were evaluated using:

* F1 Score
* Confusion Matrix
* Classification Report

The recorded best validation F1 in the notebook was:

**0.3828**

## 📁 Output

The final workflow generates a prediction file:

`submission.csv`

with:

* `User_ID`
* `Converted`

The private test prediction contains **3,000 records**.

## 🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* CatBoost
* Matplotlib
* Seaborn
* Google Colab
* Machine Learning

## 🎓 Program

Completed as part of **Summer Analytics 2026**, organized by the **Consulting & Analytics Club, IIT Guwahati**.
