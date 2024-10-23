# classification-challenge
Module 13 Challenge
# Spam Detection with Logistic Regression and Random Forest Classifier

## Overview

This project involves building a machine learning model to classify messages as **spam** or **non-spam**. The dataset used for this classification contains features that represent different aspects of messages, and the label column ("spam") specifies whether a message is spam (1) or not spam (0).

The models used for classification are:
- **Logistic Regression**
- **Random Forest Classifier**

The goal of this project is to train and evaluate these models and compare their performance in terms of accuracy and other relevant metrics.

## Data

The dataset used in this project is publicly available at:
[Spam Data CSV](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv)

### Data Description

The dataset contains multiple feature columns representing various aspects of messages, such as word frequencies, and a target column (`spam`):
- **Features (X)**: Various numerical columns that describe different characteristics of the messages.
- **Label (y)**: The `spam` column where:
  - **0** = Not spam
  - **1** = Spam

### Data Preprocessing

Before training the models, the following preprocessing steps were applied:
- **Data Splitting**: The data was split into training and testing sets using `train_test_split`.
- **Feature Scaling**: The features were scaled using `StandardScaler` to improve the performance of models that rely on distance-based calculations (e.g., Logistic Regression).

## Models Used

### Logistic Regression
The Logistic Regression model was trained using the scaled training data and evaluated using the test set. The following steps were followed:
- Fitted the model on the scaled training data.
- Made predictions on the test data.
- Calculated the accuracy score: **0.9227**

### Random Forest Classifier
The Random Forest model was also trained using the scaled training data and evaluated similarly. The steps were:
- Fitted the model on the scaled training data.
- Made predictions on the test data.
- Calculated the accuracy score: **0.9583**

### Comparison of Model Performance

| Model                 | Accuracy  |
|-----------------------|-----------|
| Logistic Regression    | 0.9227    |
| Random Forest Classifier | 0.9583    |

As predicted, the **Random Forest Classifier** performed better than the Logistic Regression model, with a higher accuracy score. This can be attributed to Random Forest's ability to handle complex patterns and interactions in the data more effectively.

## Conclusion

The Random Forest model outperformed the Logistic Regression model in detecting spam messages with an accuracy of **95.83%**, compared to **92.27%** for Logistic Regression. This result aligns with the prediction that Random Forest would better handle the complexity of the data.

## Technologies Used

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **Scikit-learn** (Logistic Regression, Random Forest, Standard Scaler)

## How to Run the Project

1. Clone the repository or download the project files.
2. Install the required libraries by running:
   ```bash
   pip install -r requirements.txt
