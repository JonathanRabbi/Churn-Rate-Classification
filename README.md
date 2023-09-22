<<<<<<< HEAD
<<<<<<< HEAD
=======
# Churn-Rate-Classification
=======
# Customer Churn Rate Classification/Clustering


![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/6c25eeb3-20bc-431e-a3ca-9673e5b088b3)

>>>>>>> afb2d7d (Update README.md)

<h2 id="table-of-contents">:book:Table of Contents</h2>
<details open="open">
  <summary>Table of Contents</summary>
<ol>
<li><a href="#Goal-of-the-Analysis"> ➤ Goal of The Analysis</a></li>
<li><a href="#Requirements"> ➤ Requirements</a></li>
<li><a href="#Dataset"> ➤ Dataset</a></li>
<li><a href="#Exploratory-Data-Analysis"> ➤ Exploratory Data Analysis</a></li>
<li><a href="#Classification"> ➤ Classification</a></li>
<li><a href="#Clustering"> ➤ Clustering</a></li>
<li><a href="#Summary-Results"> ➤ Summary Results</a></li>
<li><a href="#Time-Schedule"> ➤ Time Schedule</a></li>
</ol>
</details>

## Goal of The Analysis
A financial institution is interested in analyzing its client database to increase the revenue generated from credit cardholders. They are concerned about customers closing their bank accounts after accepting products from other institutions.
The churn rate is above 15% and increasing, the CEO urges the marketing team to start a marketing campaign for client retention.

Task:

Predict those clients with more propensity to close their bank account with the financial institution
Find possible groups of clients and define their characteristics. This will help the marketing team to design custom-made campaigns to increase customer retention.

## Dataset
The dataset can be downloaded on the following link:

[Credit Card Customers](https://www.kaggle.com/sakshigoyal7/credit-card-customers)

## Requirements
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try) <br>

> - Numpy
> - Seaborn
> - Matplotlib
> - Sklearn

## Exploratory Data Analysis
### Attrition Rate
The dataset exhibits an attrition rate of approximately 16%, indicating an imbalance. Consequently, it is essential to develop a more comprehensive evaluation framework for the model.

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/f61edc5b-efcd-4fba-95f8-38f91e2cd6f1)


### Correlation Matrix (Heatmap)
Based on the correlation matrix, we can see that Avg_Open_To_Buy & Client_Limit; Total_Trans_Cnt & Total_Trans_Amnt  are highly correlated with one-another and could thus reduce the model's accuracy.
Hence, I will be removing one of the respective features for model classification.

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/f73f5a94-9ab9-4706-843a-a3e19f8f6958)

### Scatterplots
The scatterplots can already produce an indication of certain classification features and their patterns

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/476b24f7-8606-4c6f-9ce2-fba28aedfbbc)

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/2e83ac43-b690-4c48-806d-7731cde5eac1)

## Classification
### Classifier
After partitioning my dataset into training and testing sets, the next steps involve cross-validation and hyperparameter tuning. To determine the most suitable classifier and optimal parameter values, I will utilize the GridSearchCV function from the Scikit-Learn library.

Model to choose:
- KNN
- Logistic Regression
- <b>RandomForest</b>
- DecisionTree

### Model Prediction
After selecting RandomForest with 100 estimators, my classification model achieved an accuracy score of approximately 90%. However, due to the dataset's imbalance, it is necessary to employ more robust evaluation metrics, such as:

- Confusion Matrix
- Classification Report

### Confusion Matrix
The confusion matrix indicates that my:
TN = 2120
TP = 267
FN = 18
FP = 127

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/b923b6a1-4981-4040-8a7d-e179e072eaba)


### Classification Report
The f1-score indicated a 79% accuracy level for classifying the attrited customers

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/c9a06e41-c4dc-4c07-839d-30d12be184c9)

## Clustering
### K-Means Clustering
Find the amount of clusters by means of elbow graph. Herein either 2 or 5 clusters can be chosen.

![image](https://github.com/JonathanRabbi/Credit-Card-Attrition/assets/135423708/e065b38c-5c37-4b2d-b653-645ea2307120)

## Summary Results

### Classification
In employing the RandomForest classifier with 100 estimators, the model achieves an accuracy rate of approximately 79% for identifying attrited customers. However, my primary concern lies in minimizing false positives (FP) to prevent classifying existing customers as attrited. To address this, I've focused on the F1-score, which indicates a precision level of around 68%.

### Clustering
After employing K-means and DBSCAN clustering methods to determine the more accurate cluster model, the results are as follows:
- K-means Silhouette score: ~24%
- DBSCAN Silhouette score: ~28%


## Time Schedule
This project took place between 18/09/2023-22/09/2023















>>>>>>> 0ee7e2a (Update README.md)
