# Day 05 – Student Performance Prediction: Model Comparison

## Objective

The objective of this project is to compare the performance of multiple Machine Learning classification algorithms for predicting whether a student is likely to **Pass** or **Fail** based on academic performance and attendance.

---

## Problem Statement

Educational institutions can use Machine Learning to identify students who may need additional academic support. In this project, two classification models were trained and compared to determine which one performed better in predicting student performance.

---

## Dataset

The dataset contains student academic records with the following features:

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

### Target Variable

* **1 = Pass**
* **0 = Fail**

---

## Features Used

The following features were used for model training:

* Age
* Gender
* Course
* Attendance
* Assignment Score
* Midterm Score
* Final Score

The target variable was **Result**.

---

## Data Preprocessing

The following preprocessing steps were completed before training the models:

* Loaded the dataset using Pandas.
* Explored the dataset structure and summary statistics.
* Checked for missing values.
* Filled missing numerical values using the median.
* Filled missing categorical values using the most frequent value.
* Removed duplicate records (if present).
* Separated numerical and categorical features.
* Applied One-Hot Encoding to categorical variables.
* Applied StandardScaler to numerical features.
* Built a Scikit-learn preprocessing pipeline using `Pipeline` and `ColumnTransformer`.

---

## Machine Learning Models

Two classification algorithms were trained and compared:

1. Logistic Regression
2. Decision Tree Classifier

Both models were trained using the same preprocessing pipeline to ensure a fair comparison.

---

## Model Evaluation

The models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

### Model Comparison

| Model               | Accuracy | Precision |  Recall | F1 Score |
| ------------------- | -------: | --------: | ------: | -------: |
| Logistic Regression |  100.00% |   100.00% | 100.00% |  100.00% |
| Decision Tree       |  100.00% |   100.00% | 100.00% |  100.00% |

---

## Visualizations

The notebook includes the following visualizations:

* Distribution of Pass vs Fail
* Attendance vs Final Score
* Confusion Matrix
* Model Comparison Bar Chart

---

## Analysis

Both Logistic Regression and Decision Tree achieved identical evaluation results on the test dataset.

The target variable (**Result**) was derived from student performance scores, resulting in a strong relationship between the input features and the target variable. Because of this relationship, both models were able to classify the test data with perfect performance.

Although both models achieved the same evaluation metrics, it is important to evaluate Machine Learning models using multiple metrics such as Precision, Recall, and F1 Score instead of relying only on Accuracy.

---

## What I Learned

After completing this project, I learned how to:

* Prepare a dataset for Machine Learning.
* Clean and preprocess data using Scikit-learn.
* Build reusable preprocessing pipelines.
* Train multiple classification models.
* Generate predictions on unseen data.
* Evaluate models using Accuracy, Precision, Recall, F1 Score, and Confusion Matrix.
* Compare different Machine Learning models using evaluation metrics.
* Interpret model performance instead of relying only on accuracy.
* Present model comparison results using tables and visualizations.

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

This project demonstrates a complete Machine Learning model comparison workflow, including data preprocessing, model training, prediction, evaluation, visualization, and performance analysis. It strengthened my understanding of classification algorithms, preprocessing pipelines, and the importance of using multiple evaluation metrics when comparing Machine Learning models.
