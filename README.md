# Stroke Prediction Analysis

## Topic
 - The topic we chose for our capstone project was predicting strokes. Every year more than 795,000 people in the United States has a stroke, and in 2018, 1 out of every 6 deaths from cardiovascular disease was due to stroke. This is an issue that we felt was important to explore and see what factors contribute the most to having a stroke. Some of the questions we want to answer in this analysis are:
   - How likely someone is to suffer a stroke based on gender, age, hypertension, heart disease, bmi, smoking status, average glucose level, if they were ever married, what type of work they do, and where they reside- rural or urban?
   - How all of these variables are correlated to suffering a stroke?
   - Which variable in our analysis has the most influence on having a stroke?
   - source of stroke information: https://www.cdc.gov/stroke/facts.htm

## Communication Plan
 - To accomplish our task, the most important requirement is communication between our team members. We communicate using slack, creating zoom chats weekly to go over where we are and what needs to be done, and working together during class time to delineate responsibilities that each person can then go and accomplish on their own. 

## Database
 - We have to be able to store and share our data that we will use collectively in a public database that everyone has access to. We have taken our dataset from Kaggle in CSV format, imported that data as a table in a SQLite Database, then upload it to DBHub.io and make it public with all of our team members. This allows every team member to download that database to use in our analysis and machine learning modeling. 
 - Data source: https://www.kaggle.com/fedesoriano/stroke-prediction-dataset

## Machine Learning Model
 - We will use Machine Learning on our data to answer our desired questions about strokes. Both the Support Vector Machine (SVM) and Logistical Regression models that we will use offer high accuracy with minimal computing power needed. To use our models we will first take in data from our database and Extract Transform and Load (ETL) our data, standardize that data, seperate the dataset into X(features) and y(target), split the dataset into training and test sets, import our SVC module from Scikit-Learn to train our model, then create our predictions with the model, and finally assess accuracy score. 

## Summary
 - Our group will work together to answer questions about a topic that is the fifth leading cause of death in the US: Strokes. Whether its for your own health or you know a loved one that's been affected, stroke science is imperative to know. Being able to predict a stroke based on different variables will give everyone an advantage in being able to prevent them as best we can. 
> "Knowledge itself is power" - Sir Francis Bacon
