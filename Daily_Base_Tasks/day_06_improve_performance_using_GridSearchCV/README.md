# Day 06 – Feature Engineering and Hyperparameter Tuning

## Objective

The objective of this task was to improve the Student Performance Prediction model by applying feature engineering, preprocessing, feature scaling, and hyperparameter tuning using `GridSearchCV`.

The tuned model was compared with the baseline Decision Tree model from the previous task.

---

## Problem Statement

The goal of this project is to predict whether a student is likely to **Pass** or **Fail** based on student academic performance and attendance-related information.

The project focuses on improving the Machine Learning workflow by optimizing the model's hyperparameters and evaluating whether tuning improves its performance.

---

## Dataset

The dataset contains student performance information including:

* Student ID
* Student Name
* Age
* Gender
* Course
* Attendance
* Assignment Score
* Midterm Score
* Final Score
* Result

### Target Variable

* `1` = Pass
* `0` = Fail

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

Student ID and Student Name were excluded because they are identifiers and do not provide meaningful information for predicting student performance.

---

## Data Preprocessing

The following preprocessing steps were performed:

* Loaded the dataset using Pandas.
* Inspected the dataset structure and data types.
* Checked for missing values.
* Checked for duplicate records.
* Separated numerical and categorical features.
* Used median imputation for numerical features.
* Used most-frequent imputation for categorical features.
* Applied StandardScaler to numerical features.
* Applied OneHotEncoder to categorical features.
* Combined preprocessing steps using `ColumnTransformer` and `Pipeline`.

---

## Feature Engineering

Feature engineering was explored to improve the representation of student performance.

Derived performance-related features were considered to provide additional information to the model while maintaining a structured preprocessing workflow.

---

## Baseline Model

The baseline model used for comparison was:

**Decision Tree Classifier**

The baseline model was trained using the preprocessing pipeline without hyperparameter optimization.

---

## Hyperparameter Tuning

`GridSearchCV` was used to search for better Decision Tree hyperparameters.

The following parameters were evaluated:

* `criterion`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`

Five-fold cross-validation (`cv=5`) was used during the grid search.

Example parameter grid:

```python
param_grid = {
    "classifier__criterion": ["gini", "entropy"],
    "classifier__max_depth": [3, 5, 7, None],
    "classifier__min_samples_split": [2, 5, 10],
    "classifier__min_samples_leaf": [1, 2, 4]
}
```

---

## Model Evaluation

Both models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

### Comparison Results

| Model                      | Accuracy | Precision |  Recall | F1 Score | ROC-AUC |
| -------------------------- | -------: | --------: | ------: | -------: | ------: |
| Decision Tree              |  100.00% |   100.00% | 100.00% |  100.00% | 100.00% |
| GridSearchCV Decision Tree |  100.00% |   100.00% | 100.00% |  100.00% | 100.00% |

---

## Model Comparison

Both the baseline Decision Tree and the tuned Decision Tree produced identical results on the test dataset.

The baseline model achieved:

* Accuracy: **100%**
* Precision: **100%**
* Recall: **100%**
* F1 Score: **100%**
* ROC-AUC: **100%**

After hyperparameter tuning with GridSearchCV, the tuned model also achieved:

* Accuracy: **100%**
* Precision: **100%**
* Recall: **100%**
* F1 Score: **100%**
* ROC-AUC: **100%**

Therefore, hyperparameter tuning did **not improve the test-set performance** in this particular experiment.

---

## Why Did Tuning Not Improve the Model?

The perfect performance should be interpreted carefully.

The `Result` target in this dataset is directly related to the students' `Final Score`, while `Final Score` is also included among the model features.

This creates a strong relationship between an input feature and the target variable and can result in **data leakage**.

Therefore, the models can easily learn the relationship between Final Score and Pass/Fail.

Because the baseline model was already achieving perfect performance, there was little or no room for GridSearchCV to improve the test-set metrics.

This is an important Machine Learning lesson: **a higher evaluation score does not always mean a better or more realistic model. Dataset design and feature-target relationships must also be examined.**

---

## Visualizations

The project includes visualizations for:

* Baseline vs Tuned Model Performance
* Confusion Matrix
* ROC Curve

These visualizations were used to better understand and compare model performance.

---

## What I Learned

Through this task, I learned how to:

* Prepare and clean a dataset for Machine Learning.
* Perform feature selection.
* Perform basic feature engineering.
* Build preprocessing pipelines.
* Apply feature scaling.
* Train a baseline Decision Tree model.
* Understand Machine Learning hyperparameters.
* Use `GridSearchCV` for hyperparameter optimization.
* Apply cross-validation during model tuning.
* Compare baseline and tuned models.
* Evaluate classification models using Accuracy, Precision, Recall, F1 Score, and ROC-AUC.
* Understand why a tuned model does not always outperform a baseline model.
* Identify the impact of data leakage on model evaluation.
* Interpret Machine Learning results rather than relying only on accuracy.

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

This project demonstrated the process of optimizing a Machine Learning model using feature engineering and hyperparameter tuning.

Although GridSearchCV was successfully applied and identified suitable Decision Tree hyperparameters, the tuned model did not improve the evaluation metrics because the baseline model had already achieved perfect performance.

The experiment provided practical experience with model optimization, cross-validation, evaluation metrics, and the importance of identifying data leakage when interpreting Machine Learning results.
