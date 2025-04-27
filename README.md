# Customer Retention Enhancement through Predictive Analytics
As part of a job simulation for Lloyds Banking Group's Data Science & Analytics team, I tackled a customer churn prediction challenge.

## 1. Problem Statement
SmartBank aims to reduce customer churn by predicting which customers are likely to leave. To build an accurate predictive model, we need to gather relevant customer data, explore behavioural patterns through EDA, and prepare a clean, structured dataset that reveals key drivers behind churn.

## 2. Datasets Selected and Rationale
Selected all sheets from the provided Excel file Customer_Churn_Data_Large.xlsx to ensure a comprehensive view of customer behavior. These included:
- **Customer_Demographics**: Contains customer profile information such as age, gender, marital status, and income level. These demographic features help segment customers and understand churn patterns across groups.
- **Transaction_History**: Records of customer transactions with details like transaction dates, amount spent, and product categories. Transaction data reflects customer engagement and monetary value.
- **Customer_Service**: Logs of customer service interactions including interaction types, resolution status, and dates. These highlight customer satisfaction and potential pain points.
- **Online_Activity**: Includes last login date, login frequency, and service usage which are direct indicators of customer engagement.
- **Churn_Status**: Helps to predict whether the customer has churned (left the service) or not.
  
Rationale:
Combining these datasets provides a holistic view of each customer’s profile, financial behavior, service experience, and engagement - all critical factors influencing churn.

## 3. Domain Analysis and Attributes
- **CustomerID**: Unique identifier for each customer.
- **Age**: Customer’s age.
- **Gender**: Customer’s gender.
- **MaritalStatus**: Customer’s marital status (e.g., single, married).
- **IncomeLevel**: Customer’s income bracket (e.g., low, medium, high).
- **TransactionID**: Unique identifier for each transaction made by the customer.
- **TransactionDate**: Date when a transaction occurred.
- **AmountSpent**: Amount of money spent in a transaction or period.
- **ProductCategory**: Category of product purchased.
- **InteractionID**: Unique identifier for customer service interactions.
- **InteractionDate**: Date of customer interaction with support or service.
- **InteractionType**: Type of interaction (e.g., complaint, inquiry).
- **ResolutionStatus**: Outcome of the interaction (e.g., resolved, unresolved).
- **LastLoginDate**: Date of last login or service use.
- **LoginFrequency**: How often the customer logs in or uses the service.
- **ServiceUsage**: Digital channels through which customers interact with and access their banking services.
- **ChurnStatus**: Target variable indicating whether the customer has churned (left the service) or not.

## 4. Project Workflow
### Visualizations and Statistical Summaries from EDA
- Churn does not seem to be heavily influenced by age, as churned customers are evenly spread across all ages. 
- Customers who spend less are more likely to churn.
- Customers with lower login frequency are more likely to churn.
- Slightly higher count of females (F) compared to males (M) and Churn is similar across both genders.
- Highest counts for "Widowed" and "Divorced" statuses and Churn is similar across all categories, maybe slightly higher for "Divorced".
- Churn seems to be more common in "Low" and "Medium" income levels.
- Highest counts for "Books", "Electronics" and "Clothing" products and Churn is similar across all product categories, maybe slightly higher for "Electronics".
- Complaints are strong churn predictors.
- Unresolved issues are more likely to churn.
- Higher counts for "Online Banking" and Churn risk is lower.

### Cleaned and Preprocessed Data 
- Identifying any null values
- Removing duplicates
- Identifying corrupted data
- Detecting outliers
- Checking data distribution skewness
- Encoding categorical variables,
- Feature selection
- Feature scaling
- Data splitting
- Addressing class imbalance.

### Machine Learning Models
The project implements multiple machine learning models & one deep learning model for multi-class classification:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- K-Neighbors Classifier(KNN)
- Support Vector Classifier(SVC)
- Multi-layer Perceptron (MLP) Classifier

### Hyperparameter Tuning
- GridSearchCV is used to optimize model parameters.

### Model Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report

## 5. Business Utilization
- Identify customers at risk of churn.
- Enable proactive retention strategies(personalized offers, targeted campaigns).

## 6. Potential Improvements
- Retrain model periodically with new data.
- Incorporate additional behavioral features.

## Conclusion
This project demonstrates that machine learning models - particularly **Gradient Boosting** model can accurately predict customer churn. These insights will help Lloyds Banking Group reduce attrition and boost customer lifetime value through informed, data-driven strategies.
