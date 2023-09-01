# Sparkify (A capstone project of the Datascience Nanodegree by Udacity)
## Overview:

This project focuses on developing a robust customer churn prediction model using PySpark within a data-driven business context. The goal is to effectively predict customer churn and enable data-centric decision-making. This README provides an overview of the project, its components, and key findings.

## Table of Contents:

1. [Library Used](#library-used)
2. [Introduction](#introduction)
3. [Input Data](#input-data)
4. [Data Preprocessing and Feature Engineering](#data-preprocessing-and-feature-engineering)
5. [Modeling and Evaluation](#modeling-and-evaluation)
6. [Results](#results)
7. [Conclusion](#conclusion)
8. [Acknowledgment](#acknowledgment)
9. [Improvements](#improvements)

## 1. Library Used:
The following library were used in this project

matplotlib==2.1.0<br>
numpy==1.12.1<br>
pandas==0.23.3<br>
pyspark==2.4.3<br>
seaborn==0.8.1<br>

## 2. Introduction:

In today's data-driven business landscape, predicting customer churn is crucial for effective customer relationship management. This project aims to construct a robust customer churn prediction model using PySpark, a powerful distributed data processing library. The workflow encompasses data loading, cleaning, exploratory data analysis (EDA), feature engineering, and model evaluation.

## 2. Input Data:

The project utilizes the Sparkify Project Workspace from Udacity, providing a curated environment for developing the churn prediction model. The dataset is a subset of the full 12GB dataset (128MB) and contains event data in JSON format, capturing user interactions with the Sparkify music streaming service. It includes variables such as user attributes, timestamps, session information, and activity events.

## 3. Data Preprocessing and Feature Engineering:

To prepare the data for modeling, several custom transformers and preprocessing steps are employed:

- **FilterInvalidUser:** This step removes entries with invalid authentication statuses, specifically filtering out "Logged Out" or "Guest" authentication.

- **CalculateDate:** Timestamps and registration data are converted to appropriate formats. Additionally, features such as activity timestamps, activity dates, registration timestamps, registration dates, length of stay in hours, and length of stay in days are computed.

- **GenerateAggregatedFeatures:** Rolling window features are created, including session count and total time spent.

- **get_churn_flag:** Users are labeled as churned or not based on the presence of a "Cancellation Confirmation" page in their activity. This information is incorporated into the main DataFrame.

## 4. Modeling and Evaluation:

The dataset is split into training and testing sets, with 70% of the data allocated for training. Three machine learning models are trained and evaluated:

1. **Decision Tree Classifier**
2. **Random Forest Classifier**
3. **Gradient Boosted Tree Classifier (GBT)**

Hyperparameter tuning is conducted to optimize model performance using techniques like grid search. The evaluation metric chosen is the F1 score, which balances precision and recall and is well-suited for imbalanced datasets.

## 5. Results:

The project's results indicate that the Gradient Boosted Tree Classifier (GBT) performs the best, achieving an F1 score of 0.794. This score demonstrates the model's predictive accuracy and its potential for real-world applications.

## 6. Conclusion:

This project showcases the power of data-driven decision-making in customer churn prediction using PySpark. By navigating the data loading, preprocessing, feature engineering, modeling, and evaluation steps, organizations can enhance their customer retention strategies, fostering satisfaction, loyalty, and overall success.

## 7. Acknowledgment:

We extend our gratitude to Udacity for providing the data and workspace environment for comprehensive exploration. Special recognition goes to all contributors who facilitated the project's success by guiding its development and fruition.

## 8. Improvements:

Future enhancements could explore additional feature engineering avenues, such as incorporating device variables, genres played, and song completion rates. These refinements have the potential to further elevate the model's accuracy and predictive capabilities.

Article: https://medium.com/@wahyusejatiroso/predicting-customer-churn-with-pyspark-a-deep-dive-into-data-analysis-and-machine-learning-8ec12b0c9438 
