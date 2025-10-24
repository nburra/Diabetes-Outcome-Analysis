# Diabetes-Outcome-Analysis
This project performs an exploratory data analysis and predictive modeling on a diabetes dataset to determine certain factors that affect diabetes outcomes. The analysis involves examining key patient indicators such as BP, Insulin, BMI, and Age to understand their relationship with diabetes diagnosis.

## Loading the data
I loaded the data using pandas, generating a summary statistics chart to understand the data's organization and potential quality issues.

## EDA
I performed a univariate analysis of the blood pressure indicator in the data. The displayed histogram showed that there was a large amount of values between 60 and 80. This is the most common values of blood pressure in the data set and correlates to the standard of blood pressure levels which is 120/80. There are some values of 0 in the blood pressure category that are due to NULL values, this may skew the histogram.

I also performed a pairwise analysis of blood pressure and BMI to determine their correlation. It showed that people with higher BMI will tend to have higher blood pressures. However, as it is seen in the graphs, lower BMI individuals can still have stable blood pressures.

## Pre-processing
I evaluated the data for missing or invalid values and handled it using median imputation. More specifically, there contained many zeros in the skinthickness category.

## Machine Learning Pipeline
I split the data into train/test sets, encoded categorical data, and normalized numeric data. I performed hyperparameter tuning for a Support Vector Machine (SVM) classifier using Grid Search with 5-fold cross-validation. I then evaluated the scores from GridSearchCV to diagnose any bias-variance problems. The results showed that between the train and test scores, there is very little difference or variance. What this means is that the model is good at predicting if an individual has diabetes. 

I then compared KNN and DecisionTree classifiers on my dataset and evaluated model performance. When the tree model, svm, and knn model are compared it is evident that the svm model is the best at predicting diabetes as most mean accuracies is over 78%, not only that but the standard deviation across train and test is low which indicates consistency across the model. Second to this is the knn model with an accuracy score of 0.744 or 74%. The decision tree is the lowest with 69%. The decision tree had significantly lower f1 scores than knn or svm as it had 0.77 for class 0 and 0.55 for class 1. Therefore the best overall model is the svm model. In the medical industry I would advocate for the svm model, although the model itself needs a higher score than 78% mean accuracy. However, it is efficient in predicting diabetes and would be beneficial for health professionals.
