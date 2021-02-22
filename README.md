# Financial_Performance_Prediction
## Project Overview
* Objective: The objective of this project is to select the best model out of 5 classification and regression models to predict a 
customer's capability to pay off the loan based on features such as income, education level, credit history, etc.
* Data Preprocessing: 3 approaches were used to pre-process the data set for modeling steps. 3 approaches that were used are 1. significant feature selection, 2. data scaling, and 3. removing outliers and normalizing data.
* Model Performance: Linear Regression model and XGBoost performed with accuracy scores of 90.43%.
Other models (Gradient_Boost, ADA Boost, and Random Forest Classifier) performed with higher than accuracy scores of 87%.\
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]PerformanceResults.png)

## Used Resources
-**Python Version**: 3.8\
-**Python Packages**: pandas, numpy, sklearn, matplotlib, seaborn, XGBoost, plotly\
-**Data Set**: Kaggle Loan Eligibility Data Set
-**Code Reference**: Reference cited in the respective file.\

## 1. [Data Cleaning](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Exploratory%20Data%20Analysis/Exploratory%20Data%20Analysis.ipynb)(Combined with Exploratory Data Analysis)
The original data set contained missing data. Missing data were managed following the below steps:
1. Columns with missing data were identified.
2. For each column, make predictions using 5 classification models (Random Forest Classifier, Gradient Boosting Classifier, K Neighbor Classifier, Gaussian NB, and SVC).
3. Predictions of the classification model with the best accuracy score were selected.
4. Missing data were replaced with the selected predicted values.

## 2. [Exploratory Data Analysis](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Exploratory%20Data%20Analysis/Exploratory%20Data%20Analysis.ipynb)
Highlighted findings are presented below:
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]barplots.png)
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]scatterplot.PNG)
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]scatterplot2.png)

## 3. Pre-processing Approaches and Modeling
[1] Significnat Feature Selection
Significant features were selected with SelectKBest method. Steps are shown in [this notebook.](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Approach%201.%20Significant%20Feature%20Selection/Approach%231a%20-%20Dimensionality%20Reduction.ipynb)

![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]app1Features.png)
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]heatmap.png)

Significant features selected are Credit_History, Loan Amount, Applicant Income, Coapplicant Income, etc. 

Lastly, pairplot was generated to visualize how the points are distributed.
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]pairplot.png)

[2] Data Scaling
Data were scaled using standard scaler. Detailed steps are shown in [this notebook.](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Approach%202.%20Data%20Scaling/Approach%232%20-%20Scaling%20Dataset.ipynb)

[3] Removing Outliers and Nomalizing Data
This approach gave the best model performance. Some of the common important features identified by models in this approach match with those from Approach 1.
Detailed steps are shown in [this notebook.](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Approach%203.%20Outlier%20Removal%20and%20Data%20Normalization/Approach%233%20-%20Remove%20Outliers%20and%20Normalize%20Data.ipynb)

## 4. [Result Summary](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Result%20Summary.ipynb)
The results show that Approach 3 gave the best scores for all models (Linear Regression, XGBoost, Gradient Boost, ADA Boost, and Random Forest Classifier).
Among the models in Approach 3, XGBoost and linear regression gave the best accuracy scores (90.43%).
![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]PerformanceResults.png)

![](https://github.com/jbae42/Financial_Performance_Prediction/blob/main/Plots/[2]ModelScores.PNG)
