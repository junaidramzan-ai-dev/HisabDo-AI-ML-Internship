# Day 04 – Student Performance Prediction Using Machine Learning

## Objective

The objective of this project is to build a Machine Learning classification model that predicts whether a student is likely to **Pass** or **Fail** based on their academic performance and attendance.

---

## Problem Statement

This project aims to identify students who are likely to pass or fail using historical student performance data. Such predictions can help educational institutions identify students who may need additional academic support.

---

## Dataset

The dataset contains student academic information, including:

* Student ID
* Student Name
* Age
* Gender
* Course
* Attendance
* Assignment Score
* Midterm Score
* Final Score
* Result (Target Variable)

---

## Features Used

The model was trained using the following features:

* Attendance
* Assignment Score
* Midterm Score
* Final Score
* Age
* Gender
* Course

**Target Variable**

* **Result**

  * **1 = Pass**
  * **0 = Fail**

---

## Data Preprocessing

The following preprocessing steps were performed:

* Loaded the dataset using Pandas.
* Checked dataset information and summary statistics.
* Handled missing values.
* Removed duplicate records (if present).
* Separated numerical and categorical features.
* Applied **Median Imputation** to numerical features.
* Applied **Most Frequent Imputation** to categorical features.
* Applied **One-Hot Encoding** to categorical variables.
* Applied **Standard Scaling** to numerical features.
* Combined all preprocessing steps using a **Scikit-learn Pipeline**.

---

## Machine Learning Model

The following classification model was used:

* **Logistic Regression**

The preprocessing pipeline and classification model were integrated into a single Scikit-learn Pipeline for a clean and reusable workflow.

---

## Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report

### Accuracy Achieved

**Accuracy:** **100.00%**

---

## Visualizations

The notebook includes the following visualizations:

* Distribution of Pass vs Fail
* Attendance vs Final Score
* Confusion Matrix

---

## What I Learned

Through this project, I learned how to:

* Load and explore datasets using Pandas.
* Clean and preprocess data before training a model.
* Separate features and target variables.
* Split data into training and testing sets.
* Build preprocessing pipelines using Scikit-learn.
* Apply One-Hot Encoding to categorical features.
* Standardize numerical features.
* Train a Logistic Regression classification model.
* Make predictions on unseen data.
* Evaluate model performance using Accuracy Score, Confusion Matrix, and Classification Report.
* Interpret classification results and visualize model performance.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## Conclusion

This project demonstrates a complete Machine Learning classification workflow, starting from data preprocessing and feature engineering to model training, prediction, evaluation, and visualization. It strengthened my understanding of Scikit-learn Pipelines and the importance of building reproducible machine learning workflows.
