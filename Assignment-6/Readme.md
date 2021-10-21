
# Data Description

The datasets consists of several medical predictor variables and one target variable, Outcome. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

This dataset is classification problem, determining whether or not an individual has diabetes.

# Dataset

- https://www.kaggle.com/uciml/pima-indians-diabetes-database

# Tasks involved in this analysis.
- Divding the data into train and test data.
- Analysing the data by implementing pipeline to evaluate the model.
- Involving the StandardScalar and Logestic Regression.
- Checking with the confusion matrics under which this data falls (Accuracy, Precision,etc...).
- Running a Logistic Regression model with grid search cross-validation using 10 folds.
- Searching 5 different regularization strengths and 2 solvers.
- Checking which is best model and how it perform on the test set?

# Observation
**Solvers:**
- For small datasets, liblinear is a good choice, whereas sag and saga are faster for large ones.  

**Regularization strengths:**
- I have choosen these values [0.5,1.0,1.5,10,20].
- The reason behind choosing these values because smaller values specify stronger regularization.

## Why it falls under Recall Metrics?
A person having diabetis(Class-1) and the model classifying his case as No-diabetis(Class-0) comes under False Negatives.

# Summary
- Using sklearn I have splitted the data into train and test.
- Implemented the pipeline using Scalar and Logestic regression.
- I have eliminated PCA because it is a small data set. I have tried by applying PCA the accuracy got decresed.
- Values obtained, Accuracy = 0.80, Recall = 0.58 and ROC = 0.85
- Here ROC metrics value is 0.85 so this model falls under good category.
- After applying the grid search cross validation with solvers and regularizations the recall has incresed to 0.75 before it was 0.58.
