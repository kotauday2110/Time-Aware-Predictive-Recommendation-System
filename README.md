# Time-Aware-Predictive-Recommendation-System

What You’ll Buy Next & When You’ll Buy It

In this project, we approached a recommendation business problem as a predictive challenge and enhanced the traditional collaborative recommendation system. We took a recommendation system using past choices of individuals to inform future decisions and factored in time. This adjusted the traditional recommendation system from one that could be considered annoying into one that sends timely recommendations when they are wanted. We used Instacart's grocery sales data from the past two years to build our model (dataset available on Kaggle: Instacart Market Basket Analysis
).

For example, if a user buys milk every week but toothpaste only once every three weeks, a traditional recommendation system would recommend both every visit. Our predictive recommendation system instead predicts the probability of purchase based on the timing of past purchases, sending recommendations at the right intervals.

Recommendation Differences

Steps and Instructions
Data Files
Raw data files can be obtained from Kaggle :https://www.kaggle.com/datasets/yasserh/instacart-online-grocery-basket-analysis-dataset

## Feature Engineering
Our recommender system captures time-based features, unlike traditional systems. Four kinds of features are considered: user-related, item-related, user × item-related, and time-related features. Feature engineering code is available in Data Preparation.ipynb.

## Architecture

Azure Spark ML Implementation
Spark ML - Azure.ipynb contains the PySpark code to read the feature-engineered files, process them into Spark DataFrames, and run Spark ML's Random Forest algorithm to predict probabilities for the test dataset.

## Random Forest Algorithm
Random Forest is an ensemble of decision trees. The ensemble classifier aggregates individual tree predictions to generate a final prediction.

Advantage of Using Random Forest Through Spark ML on Azure
Running Random Forest on an Azure Databricks cluster allows each decision tree to be trained in parallel using Spark’s distributed in-memory computing. This enables faster and cost-effective training, with the ability to scale the cluster configuration as needed.
