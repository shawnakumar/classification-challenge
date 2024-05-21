# Spam Detection Classification Challenge

## Background

You work at an Internet Service Provider (ISP) and have been tasked with improving the email filtering system for its customers. You've been provided with a dataset that contains information about emails, classified as either spam or not spam. Your goal is to develop a supervised machine learning (ML) model that will accurately detect spam emails to filter them out of customers' inboxes.

You will create two classification models to fit the provided data and evaluate which model is more accurate at detecting spam. The models to be created are a logistic regression model and a random forest model.

## Files

Download the following files to help you get started:

- Module 13 Challenge files

## Before You Begin

Before starting the assignment, complete the following steps:

1. Create a new repository for this project called `classification-challenge`. Do not add this homework assignment to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, add the starter file `spam_detector.ipynb` from your file downloads.
4. Push these changes to GitHub or GitLab.

## Instructions

This challenge consists of the following subsections:

1. Split the data into training and testing sets.
2. Scale the features.
3. Create a logistic regression model.
4. Create a random forest model.
5. Evaluate the models.

### Split the Data into Training and Testing Sets

Open the starter code notebook and then use it to complete the following steps:

1. Read the data from [Spam Data](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv) into a Pandas DataFrame.
2. In the appropriate markdown cell, make a prediction as to which model you expect to do better.
3. Create the labels set (y) from the “spam” column, and then create the features (X) DataFrame from the remaining columns.
   - Note: A value of 0 in the “spam” column means that the message is legitimate. A value of 1 means that the message has been classified as spam.
4. Check the balance of the labels variable (y) by using the `value_counts` function.
5. Split the data into training and testing datasets by using `train_test_split`.

### Scale the Features

1. Create an instance of `StandardScaler`.
2. Fit the Standard Scaler with the training data.
3. Scale the training and testing features DataFrames using the `transform` function.

### Create a Logistic Regression Model

Employ your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the scaled training data (`X_train_scaled` and `y_train`). Set the `random_state` argument to 1.
2. Save the predictions on the testing data labels by using the testing feature data (`X_test_scaled`) and the fitted model.
3. Evaluate the model’s performance by calculating the accuracy score of the model.

### Create a Random Forest Model

Employ your knowledge of the random forest classifier to complete the following steps:

1. Fit a random forest classifier model by using the scaled training data (`X_train_scaled` and `y_train`).
2. Save the predictions on the testing data labels by using the testing feature data (`X_test_scaled`) and the fitted model.
3. Evaluate the model’s performance by calculating the accuracy score of the model.

### Evaluate the Models

In the appropriate markdown cell, answer the following questions:

1. Which model performed better?
2. How does that compare to your prediction?

## Requirements

To receive all points, your Jupyter notebook file must have all of the following:

### Split the Data into Training and Testing Sets (30 points)

- There is a prediction about which model you expect to do better. (5 points)
- The labels set (y) is created from the “spam” column. (5 points)
- The features DataFrame (X) is created from the remaining columns. (5 points)
- The `value_counts` function is used to check the balance of the labels variable (y). (5 points)
- The data is correctly split into training and testing datasets by using `train_test_split`. (10 points)

### Scale the Features (20 points)

- An instance of `StandardScaler` is created. (5 points)
- The Standard Scaler instance is fit with the training data. (5 points)
- The training features DataFrame is scaled using the `transform` function. (5 points)
- The testing features DataFrame is scaled using the `transform` function. (5 points)

### Create a Logistic Regression Model (20 points)

- A logistic regression model is created with a `random_state` of 1. (5 points)
- The logistic regression model is fitted to the scaled training data (`X_train_scaled` and `y_train`). (5 points)
- Predictions are made for the testing data labels by using the testing feature data (`X_test_scaled`) and the fitted model, and saved to a variable. (5 points)
- The model’s performance is evaluated by calculating the accuracy score of the model with the `accuracy_score` function. (5 points)

### Create a Random Forest Model (20 points)

- A random forest model is created with a `random_state` of 1. (5 points)
- The random forest model is fitted to the scaled training data (`X_train_scaled` and `y_train`). (5 points)
- Predictions are made for the testing data labels by using the testing feature data (`X_test_scaled`) and the fitted model, and saved to a variable. (5 points)
- The model’s performance is evaluated by calculating the accuracy score of the model with the `accuracy_score` function. (5 points)

## Conclusion

### Analysis of Model Performances

#### Logistic Regression Model

- **Score:** 0.9261
- **Predictions:**
  - Correctly predicted: 7 out of 10 (from the sample provided)
  - Incorrectly predicted: 3 out of 10 (from the sample provided)
- **Accuracy:** The score suggests it has a high accuracy of 92.61%.

#### Random Forest Classifier Model

- **Score:** 0.9580
- **Predictions:**
  - Correctly predicted: 16 out of 20 (from the sample provided)
  - Incorrectly predicted: 4 out of 20 (from the sample provided)
- **Accuracy:** The score indicates a higher accuracy of 95.80%.

### Expected vs. Actual Performance

As predicted, the Random Forest model outperformed the Logistic Regression model. This outcome aligns with the initial hypothesis that Random Forest would handle the complex patterns in the spam detection task better due to its ability to capture non-linear relationships and its robustness to noise and outliers.

### Detailed Evaluation

1. **Complexity and Feature Handling:**
   - **Random Forest:** With its ensemble of decision trees, it can capture intricate patterns and interactions among features, making it more suitable for the diverse and complex nature of spam detection.
   - **Logistic Regression:** Although effective for linear relationships, it may struggle with the non-linear interactions present in the dataset.
   
2. **Performance Metrics:**
   - **Accuracy:** Random Forest has a higher accuracy score, indicating better overall performance.
   - **Error Analysis:** The Random Forest model had fewer incorrect predictions compared to the Logistic Regression model, demonstrating its superior capability in distinguishing between spam and non-spam emails.

### Conclusion

The analysis confirms that the Random Forest model outperforms the Logistic Regression model for the task of spam detection in emails. Its ability to manage complex, non-linear relationships and its robustness to various feature types makes it a better choice for this specific application.

## Sources

- GitHub
- ChatGPT
- Tutors
- Class Material