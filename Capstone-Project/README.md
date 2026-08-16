
# Capstone Project — Age Group Prediction using CatBoost

## 📌 Overview

This project focuses on predicting **age groups** using health and demographic survey data.

The target variable contains two classes:

* `Adult`
* `Senior`

A **CatBoost Classifier** was trained and evaluated using a validation split.

## 📊 Dataset

The notebook contains:

* **Training data:** 1,966 records
* **Test data:** 312 records
* **Features:** 8 input features
* **Target:** `age_group`

The dataset includes variables related to health and demographic measurements such as gender, BMI, glucose-related measurements, and other survey features.

## 🔧 Data Preprocessing

The project includes:

1. Removing records with missing target values.
2. Separating features and target.
3. Handling missing numerical values using **median imputation**.
4. Splitting the data into training and validation sets.
5. Using stratification during the train-validation split.

## 🤖 Model

The main model used was **CatBoostClassifier** with:

* Iterations: `500`
* Learning Rate: `0.05`
* Depth: `6`
* Loss Function: `Logloss`
* Evaluation Metric: `F1`

## 📈 Result

The recorded weighted F1 Score on the validation set was:

**F1 Score: 0.7783**

The trained model was also used to generate predictions for the test dataset.

## 📁 Output

The notebook generates:

`submission.csv`

containing:

* `SEQN`
* `age_group`

## 🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* CatBoost
* Google Colab
* Machine Learning

## ▶️ How to Run

The project was developed in **Google Colab**.

1. Open the `.ipynb` notebook.
2. Upload the required training and test datasets.
3. Run the notebook cells sequentially.
4. The trained model generates predictions.
5. The final predictions are saved as `submission.csv`.

## 🎓 Program

Completed as part of **Summer Analytics 2026**, organized by the **Consulting & Analytics Club, IIT Guwahati**.
