#  Churn Rate Analysis - SyriaTel company


The main of this project is to predict which customers are going to switch their mobile telephone carrier. What is the chance that a customer will switch to anoither provider



##  Business Problem

Customer churn is the loss of clients. Telephone companies use customer churn rates to as abusiness metric to since the cost of retaining an existing customer is less than acquiring a new customer.

The model will help SyriaTel answer the following business questions:

- Which customer has the highest probability of switching to another provider?
- What is the reason why people are switching to other providers?
- How sure are we that the prediction is perfect, reliable.


##  Project Objectives

The idea is retaining existing customers and also help in acquiring new ones. 



##  Dataset

- **Source**: [SyriaTel Telecom Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)


##  Data Cleaning & Preprocessing

- Phone number, had no predictive implications

-Label encoding for categorical features

-Transformation of the Target Variable to 0 and 1

-Other colums droped include total day charge, total eve charge, total night charge, total intl charge as they had a perfect correlation that would lead to multicollenearity



##  Exploratory Data Analysis (EDA)

The EDA conducted was to inpect churners and non churners
No-Churn= 85.5%

Churn = 14.5%

Then Detect imbalances in the dataset per feature

##  Feature Engineerin
- 
- **Encoding**:
  - Label encoding was used for binary categorical features.



##  Modelling
The following models were trained and evaluated:

| Model                 | Accuracy | Recall | Precision | ROC-Threshold Recall Accuracy |
|----------------------|----------|--------|-----------|---------|
| Gradient Boost | 0.97    | 0.73  | 0.90     | 0.82   |
| Support Vector MAchine        | 0.92    | 0.49  | 0.87     | 0.73   |
| Random Forest  | 0.97    | 0.65  | 0.94     | 0.73   |
| K Nearest Neibour        | 0.89    | -  | -     | -   |
| Decission Tree  | 0.92    | -  | -    | -   |
| Logistic Regression | 0.87    | -  | -     | -   |



## Final Model: Gradient Boost with Threshold optimization
After extensively modeling 6 classifiers, the Gradient boost stood out to be the best. 

### Threshold Optimization Results:
- **Optimal Threshold**: `-0.5`
- **Default Recall**: `0.73`
- **Improved Recall**: `0.82`






##  Recommendation

1. Implement retention campaign like giving customers incentives and giving discount on recharges and offering more talk time.



## Limitation

1.The data was imabalnced so the most of the models were imabalanced towards the majority class



##  Next Steps

1. Model performance optimization (fine tuning threshold) base don business requirements

2. Use |SMOTE to address class imbalance



