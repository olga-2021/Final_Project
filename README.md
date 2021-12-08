# Stroke Prediction Analysis

## Topic
 - The topic we chose for our capstone project was predicting strokes. Every year more than 795,000 people in the United States has a stroke, and in 2018, 1 out of every 6 deaths from cardiovascular disease was due to stroke. This is an issue that we felt was important to explore and see what factors contribute the most to having a stroke. Some of the questions we want to answer in this analysis are:
   - How likely someone is to suffer a stroke based on gender, age, hypertension, heart disease, bmi, smoking status, average glucose level, if they were ever married, what type of work they do, and where they reside- rural or urban?
   - What age bracket should be the most concerned with the risk of having a stroke?
   - Which variable in our analysis has the most influence on having a stroke?
   - source of stroke information: https://www.cdc.gov/stroke/facts.htm
 - After getting our data, we performed some preliminary data exploration on it to describe its characteristics including size, quantity, and accuracy of the data. We went from 5110 rows of data to 5109 due to dropping one row that had an unknown gender. We also didn't want NaN values in our BMI column, so we replaced the NaN values with the median so as to not drop a large percentage of our rows. This can be seen in the steps below:
<img width="937" alt="Screen Shot 2021-11-28 at 8 32 02 PM" src="https://user-images.githubusercontent.com/86524863/143795570-82bd641a-175c-4e78-86a5-7deef3b56ab1.png">
 
 - We also counted our unique rows in gender and did some analysis on the types of data we had as seen below:
<img width="437" alt="Screen Shot 2021-11-28 at 8 33 49 PM" src="https://user-images.githubusercontent.com/86524863/143795675-f82faec5-a3ef-4a5a-ad25-3fc5eb3bc1c0.png">

 - To further analyze our data we performed some visualizations, starting off with a distribution of predicted values as seen below:
<img width="992" alt="Screen Shot 2021-11-28 at 8 38 02 PM" src="https://user-images.githubusercontent.com/86524863/143795895-f1ddb56a-6024-4bc3-87cd-3db75047fdaa.png">

 - Next we included a visualization of the correlation between certain variables and strokes as seen below:
<img width="1067" alt="Screen Shot 2021-11-28 at 8 40 12 PM" src="https://user-images.githubusercontent.com/86524863/143796059-0ef93f82-3106-4c57-83b6-8f5165fe3837.png">

 - Finally we performed visualizations using a multitude of variables to see how the variables predicted having a stroke vs not:
 <img width="760" alt="Screen Shot 2021-11-28 at 8 41 38 PM" src="https://user-images.githubusercontent.com/86524863/143796269-8ceee92d-e437-495a-834a-4bb886621403.png">

## Database- William Richardson
 - We have to be able to store and share our data that we will use collectively in a public database that everyone has access to. We have taken our dataset from Kaggle in CSV format, imported that data as a table in a SQLite Database, then upload it to DBHub.io and make it public with all of our team members. This allows every team member to download that database to use in our analysis and machine learning modeling. 
 - Data source: https://www.kaggle.com/fedesoriano/stroke-prediction-dataset
 - DBHub I/O: https://dbhub.io/wprich/Final.db
 - After reviewing the raw stroke dataset with another dataset found on kaggle relating to heart disease, it was decided that a join could be used to expand our dataset.  This was done in the hopes of either adding more variables and specifying more causes to heart disease/stroke in general or just adding more data to our dataset to ensure better testing of our statistical models. Doing a "LEFT OUTER JOIN" on the two tables on various columns, it was decided that the heart data set could not be used and we would stick with the original plan of using the raw stroke dataset after cleaning the data up.
 - After cleaning up the raw stroke data into a new data set aptly named clean stroke data, it was then added to the database as another table.  This was done for comparisons among the two and to also keep a record for any/all discrepancies that may arise. A ERD, or Entity Relationship Diagram, was then created out of those two data sets.  This was done to see which columns were still there and to also ensure that nothing was accidentally dropped/deleted.  The ERD shows a clear 1 to 1 comparison in the two datasets and also that the only column dropped was the one intended, namely the "id" column. 
 - A screenshot of our database can be seen below:
<img width="1264" alt="Screen Shot 2021-11-28 at 5 42 04 PM" src="https://user-images.githubusercontent.com/86524863/143789198-c10a45c1-e65d-4fc5-ade4-7772921c60cd.png">

## Machine Learning Model- Olga Postolachi
 - We will use Machine Learning on our data to answer our desired questions about strokes. Both the Support Vector Machine (SVM) and Logistical Regression models that we will use offer high accuracy with minimal computing power needed. The limitations of the SVM model are that it doesn't handle large datasets very well, and the major limitation of a Logistical Regression model is that it assumes the linearity between the independent and dependent variable; keeping these in mind we turned to our analysis. To use our models we will first take in data from our database and Extract Transform and Load (ETL) our data, standardize that data, seperate the dataset into X(features) and y(target), split the dataset into training and test sets, import our SVC module from Scikit-Learn to train our model, then create our predictions with the model, and finally assess accuracy score. 
 - A screenshot of our imported dataframe can be seen below: 
<img width="940" alt="Screen Shot 2021-11-28 at 5 44 22 PM" src="https://user-images.githubusercontent.com/86524863/143789277-31130bf7-690c-4b91-96db-421512a80ed2.png">

 - We tried 5 different models- the best performing ones were SVM and Logistical Regression with an accuracy of 74% and a recall score of 79%, the worst performing one was the Random Forest Classifier with an accuracy of 91% but a recall score of only 13%.  

## Presentation- Rolland Ikponmwosa 
 - We will be using Powerpoint to present our project to classmates, and have provided a PDF in our GitHub.
 - We will be using the powerful Tableau software to visualize our data in order to present it. We will create a storyboard of different graphs and visualizations in order to answer our initial questions regarding our data. This will provide a great way for others to understand what our analysis has accomplished in a presentation setting.
 - Link to interactive Tableau Storyboard: https://public.tableau.com/app/profile/bryan.werth/viz/StrokeStory/Story1?publish=yes
[Presentation_Final.pdf](https://github.com/olga-2021/Final_Project/files/7673319/Presentation_Final.pdf)


## Summary & GitHub- Bryan Werth
 - Our group will work together to answer questions about a topic that is the fifth leading cause of death in the US: Strokes. Whether its for your own health or you know a loved one that's been affected, stroke science is imperative to know. Being able to predict a stroke based on different variables will give everyone an advantage in being able to prevent them as best we can. 
> "Knowledge itself is power" - Sir Francis Bacon.
