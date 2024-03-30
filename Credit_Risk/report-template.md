# Module 20 Report 

## Overview of the Analysis

    The purpose of this analysis is to develop a machine learning model that can predict the loan
status (healthy or high-risk) based on financial information provided in the dataset.
    The dataset contains financial information related to loans, such as loan status (healthy or
high-risk), as well as various other features such as loan size, interest rate, borrower income,
debt_to_income ratio, number of accounts, derogatory marks. The goal is to predict the loan status
based on these features.
    Let's provide basic information about the loan_status variable:
value_counts of loan_status:
0    75036
1     2500
This shows that there are 75,036 healthy loans (0) and 2500 high-risk loans (1) in the dataset.

    Stages of the Machine Learning Process:
    Data Preprocessing: 
- load the dataset; 
- read the data from Resources folder into a DataFrame;
Since all variables in our dataset are numeric, there's no need for encoding categorical variables.
I can directly use the dataset for machine learning algorithms that accept numerical input.
- separate features and labels; 
- split the data into training and testing sets;
- choose Logistic Regression machine learning algorithms;
    In this analysis, we used Logistic Regression as the machine learning algorithm. Logistic
    Regression is a popular choice for binary classification problems like this one, where the goal
    is to predict the probability of a sample belonging to a particular class.

- train the selected models using the training data;
- evaluate the performance of the trained models using various metrics such as accuracy, precision, recall, and confusion matrix;


## Results of Logistic Regression:
Accuracy: 99%
Precision:  Class 0 (Healthy loans): 100%, 
            Class 1 (High-risk loans): 85%
Recall:     Class 0 (Healthy loans): 99%, 
            Class 1 (High-risk loans): 91%



Precision: Precision measures the accuracy of the positive predictions made by the model. For class 0 (healthy loans), a precision of 1.00 means that when the model predicts a loan to be healthy, it is correct 100% of the time. For class 1 (high-risk loans), a precision of 0.85 means that when the model predicts a loan to be high-risk, it is correct approximately 85% of the time.

Recall: Recall measures the ability of the model to capture all positive instances. For class 0, a recall of 0.99 means that the model correctly identifies 99% of all healthy loans. For class 1, a recall of 0.91 means that the model correctly identifies 91% of all high-risk loans.

F1-score: The F1-score is the harmonic mean of precision and recall. It provides a balance between precision and recall. For class 0, an F1-score of 1.00 indicates a perfect balance between precision and recall. For class 1, an F1-score of 0.88 indicates a good balance between precision and recall, although it's slightly lower than class 0.

Support indicates the number of actual occurrences of each class in the test dataset.

 An accuracy of 0.99 indicates that the model correctly predicts 99% of all instances in the test dataset.

The macro average calculates the metric independently for each class and then takes the average. In this case, it averages precision, recall, and F1-score across both classes.

The weighted average calculates the metric for each class and weights it by the number of true instances of each class before averaging. It gives more weight to the metrics of the class with more instances. In this case, it averages precision, recall, and F1-score across both classes, weighted by the number of instances of each class.

## Summary
Overall, the Logistic Regression model performs exceptionally well, with high accuracy, precision, and recall scores for both classes. It correctly identifies the majority of healthy loans and maintains a good balance between precision and recall for high-risk loans. Since the goal is to predict both healthy and high-risk loans accurately, this model seems to be the best choice.

The performance of the model is crucial for both classes, but it's particularly important to correctly predict high-risk loans (class 1) to mitigate potential financial risks for the lender. The Logistic Regression model achieves a high precision score for high-risk loans, indicating that it effectively identifies most high-risk loans while minimizing false positives. Therefore, it is recommended to use the Logistic Regression model for predicting loan statuses in this analysis.




