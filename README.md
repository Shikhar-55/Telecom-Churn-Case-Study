# Telecom-Churn-Case-Study

### Telecom Churn Prediction
This project aims to analyze customer-level data from a leading telecom firm in order to build predictive models and identify customers at high risk of churn. The telecom industry experiences a high churn rate, and retaining high-profitable customers is crucial for telecom companies. By predicting churn and identifying the main indicators, companies can take proactive measures to reduce customer attrition and retain their high-value customers.

### Business Problem Overview
In the highly competitive telecom industry, customers have the freedom to choose from multiple service providers and frequently switch from one operator to another. The annual churn rate in the industry ranges from 15% to 25%. Acquiring new customers is significantly more expensive than retaining existing ones, making customer retention a top priority for telecom companies.

The objective of this project is to predict which customers are at a high risk of churn. By identifying these customers in advance, telecom companies can implement targeted retention strategies to reduce churn and retain their high-value customers.

### Understanding and Defining Churn
Churn can be defined differently based on the payment model in the telecom industry. There are two main models: postpaid and prepaid. In the postpaid model, customers inform the operator when they want to switch to another provider, making it easy to identify churn instances. However, in the prepaid model, customers can simply stop using the services without notice, making churn prediction more challenging.

For this project, churn will be defined using a usage-based approach. Customers who have not made any incoming or outgoing calls and have not used mobile internet during a specific period will be considered churned. It is important to note that churn prediction is especially critical for prepaid customers, as prepaid is the dominant model in the Indian and Southeast Asian market.

### High-Value Churn
Approximately 80% of the telecom industry's revenue comes from the top 20% of customers, known as high-value customers. Reducing churn among these customers is crucial for minimizing revenue leakage. Therefore, in this project, high-value customers will be defined based on a certain metric, and churn prediction will focus specifically on high-value customers.

### Data and Business Objective
The dataset used in this project contains customer-level information for four consecutive months: June, July, August, and September. The objective is to predict churn in the last month (September) using data from the first three months (June, July, August). Understanding typical customer behavior during churn is essential for achieving accurate predictions.

### Data Preparation
The following data preparation steps are crucial for this problem:

Filter high-value customers: High-value customers will be defined as those who have recharged with an amount greater than or equal to the 70th percentile of the average recharge amount in the first two months (June and July). This filtering will result in a dataset of approximately 30,000 rows.

Tag churners and remove churn phase attributes: Churned customers will be identified based on the fourth month (September). Customers who have not made any calls (incoming or outgoing) and have not used mobile internet in September will be tagged as churners (churn = 1), while others will be tagged as non-churners (churn = 0). All attributes corresponding to the churn phase will be removed from the dataset.

### Modelling
The predictive models built in this project will serve two purposes:

Predict whether a high-value customer will churn in the near future (churn phase) to enable proactive retention strategies, such as providing special plans or discounts on recharge.

Identify important variables that strongly predict churn, providing insights into why customers choose to switch to other networks.

To handle the class imbalance issue (typical churn rate of 5-10%), techniques for handling class imbalance will be employed. The suggested steps for building the model include
