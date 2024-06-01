# Customer Churn Prediction Project
Customer churn, the phenomenon where customers stop doing business with a company, is a critical issue for many businesses. Understanding and predicting customer churn is essential for businesses to implement effective customer retention strategies. This project aims to analyze customer churn data and build predictive models to identify customers who are likely to churn. By leveraging these predictive models, businesses can take proactive measures to improve customer retention and enhance overall business performance.

# Table of Contents

/n Project Description
Dataset
Project Structure
Results
Technologies Used
Contributing
License
Contact


# This project involves the following key steps:
Data Preprocessing: Cleaning and preparing the data for analysis.
Exploratory Data Analysis (EDA): Understanding the data through visualization and statistical analysis.
Feature Engineering: Creating new features to improve model performance.
Model Building: Developing machine learning models to predict customer churn.
Model Evaluation: Assessing the performance of the models using various metrics.
Insights and Recommendations: Providing actionable insights to reduce churn.


# Dataset
The dataset used in this project contains information about customer behavior and demographics. It includes features such as:
Customer ID
Gender
Partner
Dependents
PhoneService
MultipleLines
InternetServices 
StreamingTV
OnlineSecurity
OnlineBackup
DeviceProtection
TechSupport
StreamingMovies
Contract
PaperLessBilling
PaymentMethon
MonthlyCharges
TotalCharges
Churn
from this link (provide a link to the dataset if available online).

# Results

The results of the project include:

Exploratory Data Analysis: Visualizations and insights about the factors affecting customer churn.
- There are 7032 observation and 21 features in the dataset
- There some missing values in TotalCharges. In total, the dataset has a combination of 12 objects which are 4 numrical feature 
Object value types  are as follows Categorical:customerID,gender,Partner,Dependents,PhoneService,MultipleLines,InternetService,OnlineSecurity,DeviceProtection,TechSupport,StreamingTV,StreamingMovies,Contract,PaperlessBilling,PaymentMethod,Churn Numerical value types are:SeniorCitizen,tenure,MonthlyCharges,TotalCharges
- TotalCharges has 11 missing observation which.
- There are no duplicate values in the datasets.
- No outliers

While oberving the feature for outliers; it becomes apparent that the distributions of the variables 'tenure' and 'MonthlyCharges', are slightly left-skewed while 'TotalCharges' is extremly left-skewed. This suggests that the majority of the observations for these variables are concentrated towards the lower end of their respective ranges, with fewer instances observed at higher values.

A deeper dive shows that
Customers with higher monthly charges are more likely to churn compared to those with lower charges.
Customers on monthly subscriptions have a higher churn rate than those on one-year or two-year subscriptions.
Insights
1.	This suggests that the cost sensitivity of customers plays a significant role in their decision to leave the service. Higher monthly expenses may contribute to dissatisfaction or financial strain, leading to higher churn rates.Subscription Type and Churn
2.	Monthly subscriptions might be perceived as less committed and more flexible, making it easier for customers to cancel. Longer-term subscriptions may provide more stability and commitment, reducing the likelihood of churn. Relationship Between Tenure and Total Charges



feature important graph was also used to help identified the most important in predicting whether a user will churn or not.
From the diagram; the following five features are important in predicting whether a user will churn or not
    -Total charges 
    -Tenure 
    -Monthly charges 
    -Contact Month to Month
    -Technical support No

Insight
Total Charges: The cumulative amount a user has been billed. Higher total charges can indicate long-term engagement or higher usage, but also may reflect accumulated costs that could lead to churn.

Tenure: The duration a user has been with the service. Longer tenure often correlates with loyalty and lower churn rates, while shorter tenure may indicate a higher risk of churn.

Monthly Charges: The amount a user is billed monthly. Higher monthly charges can be a significant factor in a user's decision to churn due to the financial burden.

Contract Type: Month-to-Month: Users on a month-to-month contract tend to have higher churn rates compared to those on longer-term contracts, as there is less commitment and more flexibility to cancel.

Technical Support: No: Users who have not accessed technical support services might feel underserved or frustrated with unresolved issues, leading to a higher likelihood of churning.


# Model Performance: Evaluation metrics for different models (e.g., accuracy, precision, recall, F1-score).

Three supervised learning model was used to test and train model and then thw model was eveluated using calssification report ad confusion metrix 
Logistic regression model:
Here is the classification report for customer that are likely to churn 
Accuracy : 0.80
Precision: 0.64
Recall: 0.55
F1-score: 0:59

Customer that may likley not churn
Precision: 0.85
Recall: 0.89
F1-score: 0:87

Examining the confusion matrix provides further insight into the model's performance:
True Negatives (TN): The model correctly identified 65% of the cases where clients did churn. False Negatives (FN): The model incorrectly classified 8.25% of the non-churned clients as churned, highlighting areas for improvement.

# Decision tree model:
Here is the classification report for customer that are likely to churn 
Accuracy :0.72
Precision: 0.47
Recall: 0.52
F1-score: 0.50
 
Customer that may likley not churn
Precision:0.82
Recall: 0.79
F1-score: 0.81
Examining the confusion matrix provides further insight into the model's performance:
True Negatives (TN): The model correctly predicts 58.53% of churn cases, demonstrating reliable performance in identifying clients who remain.
False Negatives (FN): The model incorrectly classifies 15.17% of churned clients as non-churned, indicating areas where the model could be improved to better capture at-risk clients.


# Gradient boosting model:
Here is the classification report for customer that are likely to churn 
Accuracy : 0.80
Precision : 0.65
Recall : 0.50
F1-score : 0.56

Custmer that may likley not churn
Precision: 0.83
Recall: 0.90
F1-score: 0.87
Examining the confusion matrix provides further insight into the model's performance:
True Negatives (TN): The model correctly predicts 66.54% of churn cases, demonstrating reliable performance in identifying clients who remain. False Negatives (FN): The model incorrectly classifies 7.16% of churned clients as non-churned, indicating areas where the model could be improved to better capture at-risk clients.

Analyzing the confusion matrix provides deeper insights into the model's predictive capabilities:
True Negatives (TN): The model correctly predicts 66.54% of churn cases, demonstrating reliable performance in identifying clients who remain. False Negatives (FN): The model incorrectly classifies 7.16% of churned clients as non-churned, indicating areas where the model could be improved to better capture at-risk clients.

# Recommendations
Among the three models used to train and test in this project  Decision tree model shows good overall accuracy and  performs better at predicting clients who churn as compared to other model

Contributions are welcome! If you have any suggestions or improvements, please create an issue or submit a pull request.

If you have any questions or feedback, please contact me at [tolaukel@gmail.com].

