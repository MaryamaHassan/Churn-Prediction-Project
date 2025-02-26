# Customer Churn Analysis Project

## Overview
Customer churn presents a critical challenge for businesses, as keeping existing customers is often more cost-effective than acquiring new ones. This project aims to analyse customer churn using machine learning models, find key factors influencing customer retention, and offer actionable insights to mitigate churn. By using data-driven approaches, businesses can uncover patterns affecting customer decisions and adjust strategies accordingly.

## Data Loading and Exploration
The dataset is sourced from a CSV file and undergoes an initial assessment to ensure quality. This process includes:
- Identifying and handling missing values
- Detecting and removing duplicate entries
- Generating a statistical summary of the dataset

These steps provide a comprehensive understanding of the dataset’s structure and help identify any anomalies that may affect model performance.

## Data Cleaning
To ensure data integrity, a rigorous cleaning process is applied:
- **Handling missing values:** Missing data is appropriately addressed to prevent biases in model training.
- **Removing duplicate records:** Eliminating redundant entries to avoid skewed analysis results.
- **Data type conversions:** Ensuring consistency in numerical and categorical data types.

These preprocessing steps contribute to reliable insights and accurate predictions.

## Exploratory Data Analysis (EDA)
Understanding customer behaviour is essential in finding churn patterns. Various visualisations are performed to analyse key aspects of the data:
- **Churn Rate Distribution:** A pie chart illustrating the proportion of customers who have churned versus those who remain.
- **Internet Service Distribution:** An analysis of diverse types of internet services customers use and their impact on retention.
- **Tech Support Availability:** Examining whether customers with access to tech support are less likely to churn.
- **Churn vs Monthly Charges:** A bar chart highlighting the relationship between churn probability and monthly charges.
- **Churn vs Tenure:** Investigating how customer tenure influences churn likelihood.
- **Contract Type vs Monthly Charges & Age:** A comparative study of how different contract types correlate with monthly charges and customer demographics.

## Key Insights
From the analysis, several key trends appear:
- Customers with long-term contracts show lower churn rates, though fewer customers opt for two-year contracts.
- Customers with higher monthly charges are more likely to churn, suggesting price sensitivity plays a crucial role in retention decisions.
- Access to tech support and specific internet service types influence retention rates, highlighting areas businesses should focus on to enhance customer experience.

## Feature Engineering
To enhance model performance, categorical variables such as **Gender** and **Churn** are encoded into numerical representations. The most important features selected for model training include **Age, Gender, Tenure, and MonthlyCharges**. Feature importance analysis offers deeper insights into customer behaviour, ensuring that only the most relevant attributes contribute to model training.

## Data Splitting & Scaling
Before training the models:
- The dataset is split into **training (80%)** and **testing (20%)** sets.
- Standardisation is applied to numerical features to ensure consistency in model performance.
- The scaler is saved for future use, helping seamless model retraining and deployment.

## Model Training & Evaluation
Multiple machine learning models are implemented and compared:

### Logistic Regression
- Serves as a baseline model for churn prediction.
- Achieved an accuracy of **88.50%**.
- Provides insights into the weight of different features on churn likelihood.
- **AUC score:** 0.80.

### K-Nearest Neighbors (KNN)
- Trained and optimised using Grid Search.
- Achieved an accuracy of **88.00%**.
- **AUC score:** 0.79.

### Random Forest Classification
- Initially trained with default parameters, then fine-tuned using Grid Search for optimal performance.
- **Best parameters:** `{'max_depth': None, 'min_samples_leaf': 4, 'min_samples_split': 10, 'n_estimators': 200}`.
- Initial accuracy: **87.50%**, improving to **88.00%** after tuning.
- **AUC scores:** 0.84 (default) and 0.86 (tuned).

  ![Curve Output](https://github.com/user-attachments/assets/c819e2a9-dd92-4c95-9500-d7751c8bbf47)


## Feature Importance Analysis
To understand which features have the greatest impact on churn prediction, feature importance is assessed:
- **Age:** 20.14%
- **Gender:** 3.92%
- **Tenure:** 36.38%
- **MonthlyCharges:** 39.57%

**MonthlyCharges** and **Tenure** appear as the most influential factors affecting customer churn.

## Key Findings
- **Logistic Regression** provided a strong baseline performance with an accuracy of **88.50%**.
- **KNN** achieved an accuracy of **88.00%**, showing the effectiveness of similarity-based classification.
- **Random Forest** initially achieved an accuracy of **87.50%**, which improved to **88.00%** after hyperparameter tuning.
- **MonthlyCharges** and **Tenure** are the most significant factors influencing customer churn.
- Customers with **shorter tenure** and **higher monthly charges** are at the highest risk of churning.
- **Contract type** and **tech support availability** also play a crucial role in customer retention.

## Conclusion
This project successfully applies machine learning techniques to understand customer churn and identify key influencing factors. The study highlights:
- The importance of **feature selection** and **model tuning** in improving predictive performance.
- Critical insights into **customer retention strategies**, emphasising contract flexibility and pricing adjustments.
- The potential for businesses to **proactively reduce churn rates, enhance customer loyalty, and improve long-term profitability**.

### Future Enhancements:
- Expanding feature selection to incorporate additional customer demographics.
- Exploring ensemble learning techniques to improve prediction accuracy.
- Developing a real-time dashboard for businesses to monitor churn risk and take immediate action.

By using these analytical approaches, businesses can enhance their decision-making processes and improve customer retention strategies.

