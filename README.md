# Sparkify
## A capstone project of the [datascience nanodegree by Udacity]

We have an example of a virtual company called 'Sparkify' who offers paid and free listening service, the customers can switch between either service, and they can cancel their subscription at any time.

The project aims to build a machine learning model using PySpark to predict customer churn for the 'Sparkify' music streaming platform, analogous to Spotify. The dataset, a subset provided by Udacity for their Data Science Capstone project, comprises web interactions including page details, timestamps, and userIDs. While the full dataset requires powerful hardware, a smaller sample is used here. The emphasis is on scalability, favoring PySpark over pandas and scikit-learn.

This workspace contains a subset (128MB) of the full Sparkify dataset (12GB):

<b>1. Importing Libraries</b><br>
The code begins by importing necessary libraries and modules from the PySpark ecosystem, as well as other Python libraries like NumPy and pandas.

<b>2. Load and Clean Dataset</b><br>
The mini-dataset file mini_sparkify_event_data.json is loaded into a Spark DataFrame called df. Invalid or missing data are checked, particularly records without userId or sessionId. Invalid userId entries, such as "Logged Out" or "Guest," are identified and handled.

<b>3. Exploratory Data Analysis (EDA)</b><br>
In this section, exploratory data analysis is performed on the mini-dataset to understand the data better. Data quality checks are conducted, and various features are created based on user behavior.

<b>4. Define Churn</b><br>
The concept of "churn" is introduced by identifying the Cancellation Confirmation events for both paid and free users. This event will serve as the basis for defining churn.

<b>5. Explore Data</b><br>
Basic exploratory data analysis is carried out to observe the behavior of users who stayed versus users who churned. Aggregates are computed to analyze user interactions, preferences, and patterns.

<b>6. Identify Features for Churn Prediction</b><br>
Different features that might be useful for predicting churn are created. These features include:
a. Length of Stay (los_days)
b. Categorized Length of Stay (los_flag)
c. Categorized Item in Session (itemInSession_flag)
d. Categorized Length of Songs (length_flag)

<b>7. Visualize Churn Analysis</b><br>
Visualizations are created to display the churn rate based on different factors such as user level, gender, length of stay, and item in session.

<b>8. Wrapping Up<br>
The code concludes by displaying a portion of the DataFrame to give you an idea of the data structure.

Feel free to use this code as a starting point to develop your Sparkify project further. You can explore advanced machine learning techniques, feature engineering, model training, and evaluation to predict user churn effectively. Good luck with your Sparkify project!
