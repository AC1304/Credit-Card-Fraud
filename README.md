# Credit Card Fraud Detection  
**FindDefault (Predicting Credit Card Fraud)**  
The dataset for this project can be downloaded via the following link: [creditcard.csv](https://kh3-ls-storage.s3.us-east-1.amazonaws.com/DS%20Project%20Guide%20Data%20Set/creditcard.csv)

## Problem Statement  
The objective of this project is to predict fraudulent credit card transactions using machine learning models.

In this analysis, we will work with customer-level transaction data collected through a collaboration between Worldline and the Machine Learning Group.

The dataset, sourced from Kaggle, consists of 284,807 transactions, of which 492 are fraudulent. Given the high imbalance in the dataset, appropriate handling of this imbalance is necessary before building the model.

## Business Problem Overview  
Retaining profitable customers is a key goal for banks. However, banking fraud presents a major threat to this goal. Fraudulent activity leads to significant financial losses, damages to trust and credibility, and concerns for both banks and their customers.

According to a Nilson Report, it is estimated that by 2020, banking fraud would result in losses of $30 billion globally. As digital payment channels continue to grow, the number of fraudulent transactions also rises, with new and evolving methods of fraud.

In the banking industry, detecting credit card fraud using machine learning is no longer just a trend—it's essential for enabling proactive fraud prevention and monitoring. Machine learning helps financial institutions reduce manual reviews, costly chargebacks, fees, and the denial of legitimate transactions.

## Understanding and Defining Fraud  
Credit card fraud refers to any dishonest activity aimed at obtaining information or making unauthorized transactions for financial gain. One of the most common forms of fraud is skimming, where the information on a card's magnetic strip is duplicated. Other types of fraud include:

- Manipulation or alteration of genuine cards  
- Creation of counterfeit cards  
- Theft of lost or stolen credit cards  
- Fraudulent telemarketing  

## Data Dictionary  
The dataset contains credit card transaction records from European cardholders over a two-day period in September 2013. Out of the total 284,807 transactions, 492 are fraudulent. The dataset is highly imbalanced, with fraudulent transactions making up only 0.172% of the total. To protect privacy, the dataset has been transformed using Principal Component Analysis (PCA). Except for the ‘time’ and ‘amount’ features, all other features (V1, V2, V3, up to V28) represent principal components derived via PCA. 

- **Time**: The number of seconds elapsed between the first transaction and subsequent transactions.  
- **Amount**: The transaction amount.  
- **Class**: The target variable indicating fraud (1) or non-fraud (0).

## Data Understanding  
At this stage, we need to load the dataset and gain a deep understanding of its features. This will guide our selection of relevant features for the final model.

## Exploratory Data Analysis (EDA)  
In this step, we perform univariate and bivariate analyses of the dataset. We may also conduct feature transformations if necessary. Since Gaussian variables are used in this dataset, Z-scaling is not required. However, we should check for skewness and address it if found, as it may impact the model’s performance.

## Train/Test Split  
Once we’re familiar with the dataset, we can split the data into training and testing sets to evaluate the performance of our models on unseen data. For validation, we will use k-fold cross-validation. We must ensure that the value of *k* is chosen appropriately so that the minority class (fraudulent transactions) is well-represented in the test folds.

## Model Building and Hyperparameter Tuning  
This phase involves trying out different machine learning models and fine-tuning their hyperparameters to achieve the desired performance. We will also explore various sampling techniques to improve the model’s effectiveness.

## Model Evaluation  
We will evaluate the models using appropriate metrics. Since the dataset is imbalanced, the primary goal is to accurately identify fraudulent transactions rather than non-fraudulent ones. Therefore, we need to select evaluation metrics that best reflect this business priority.
