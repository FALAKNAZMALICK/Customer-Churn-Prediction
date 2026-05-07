# Customer-Churn-Prediction
Enhanced customer churn prediction using the Churn Modelling Dataset with Random Forest, feature scaling, and one‑hot encoding. Includes EDA, visualization, and feature importance analysis to identify key drivers of churn.

## Objective
Identify customers who are likely to leave the bank (churn) using demographic and financial data. This classification task helps banks understand customer behavior and reduce attrition.

## Dataset
The project uses the **Churn Modelling Dataset**, which contains customer details such as:
- Credit Score  
- Geography  
- Gender  
- Age  
- Balance  
- Estimated Salary  
- Exited (Target variable: 1 = churn, 0 = retained)

## Approach
1. **Data Loading & Cleaning**
   - Loaded dataset (`Churn_Modelling.csv`) using pandas
   - Dropped irrelevant identifiers (`RowNumber`, `CustomerId`, `Surname`)

2. **Data Encoding**
   - Applied one-hot encoding to categorical features (`Geography`, `Gender`)

3. **Feature Scaling**
   - Standardized numerical features (Balance, Salary, etc.) using `StandardScaler`
   - Improved model performance on features with large numeric ranges

4. **Model Training**
   - Split dataset into training (80%) and testing (20%)
   - Trained a Random Forest Classifier with 100 estimators

5. **Model Evaluation**
   - Measured accuracy score
   - Visualized confusion matrix with heatmap
   - Generated classification report for precision, recall, and F1-score

6. **Feature Importance**
   - Ranked top factors influencing churn
   - Visualized top 10 features using bar plots

## Results & Insights
- **Model Accuracy:** Achieved approximately **86.65%**   
- **Key Drivers of Churn:** Age, balance, credit score, and geography were among the strongest predictors.  
- **Business Insight:** Customers with lower balances and certain geographic profiles showed higher churn risk.  
- Random Forest provided robust performance and interpretable feature importance.
