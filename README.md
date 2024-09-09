# Loan Approval Prediction using MongoDB and Azure ML Studio

## Project Overview

This project demonstrates how to predict loan approval status using a machine learning model built in **Azure ML Studio** with data stored in **MongoDB Atlas**. The goal of this project is to provide an end-to-end machine learning solution that integrates data ingestion from MongoDB with model training and evaluation in Azure ML Studio.

## Project Workflow

1. **Data Ingestion**: Data is retrieved from a MongoDB Atlas cluster using the `pymongo` driver.
2. **Data Preprocessing**: Data is cleaned and preprocessed, including handling missing values, encoding categorical variables, and scaling numerical features.
3. **Modeling**: Multiple machine learning models are trained, including Logistic Regression, Support Vector Classifier (SVC), and Random Forest. Hyperparameter tuning is performed using `RandomizedSearchCV`.
4. **Model Saving**: The best-performing model (Random Forest) is saved using `joblib` for future predictions.
5. **Model Deployment** (Optional): The model could be deployed on Azure for real-time predictions (deployment not done in this project).
6. **Predictions**: The saved model is used to predict loan approval for new data.

## Prerequisites

To run this project, you need the following:

- A **MongoDB Atlas** cluster for data storage.
- **Azure ML Studio** setup for model training.
- **Python 3.x** and the following libraries:
  - `pandas`
  - `numpy`
  - `sklearn`
  - `pymongo`
  - `joblib`
 
## Results

- **Logistic Regression Accuracy**: 80.48% (after hyperparameter tuning)
- **Support Vector Classifier (SVC) Accuracy**: 80.66% (after hyperparameter tuning)
- **Random Forest Accuracy**: 80.66% (after hyperparameter tuning)

Among the models tested, both the **Support Vector Classifier** and **Random Forest** achieved the highest accuracy of 80.66%. However, the **Random Forest** model was selected for final predictions due to its better balance between precision and recall.
