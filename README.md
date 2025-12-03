# Telco Customer Churn Prediction

## 📌 Overview
This project predicts **customer churn** for a telecom company using machine learning.  
It demonstrates a complete **data science workflow**: data cleaning, preprocessing, feature engineering, modeling, evaluation, and business insights.

## 📊 Dataset
- Source: [Kaggle - Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)  
- Size: 7043 rows, 21 columns  
- Key features:
  - Customer demographics (gender, senior citizen, partner, dependents)
  - Account info (tenure, contract, payment method, monthly charges, total charges)
  - Services (phone, internet, streaming, tech support)
  - Target: `Churn` (Yes/No)

## 🛠 Methodology / Steps
1. **Data Understanding**
   - Explored dataset structure, missing values, distributions, and class imbalance.
2. **Data Cleaning & Preprocessing**
   - Fixed `TotalCharges` column
   - Dropped `customerID`
   - Encoded categorical variables (One-Hot + Label Encoding)
   - Scaled numeric features
3. **Exploratory Data Analysis (EDA)**
   - Visualized churn distribution, tenure, monthly charges
   - Correlation heatmaps and insights
4. **Handling Class Imbalance**
   - Used **SMOTE** to balance the target classes
5. **Train-Test Split**
   - 80/20 split for training and testing
6. **Modeling**
   - Logistic Regression (baseline)
   - Random Forest Classifier (advanced)
7. **Model Evaluation**
   - Accuracy, AUC, Confusion Matrix, Classification Report
   - ROC Curve comparison
   - Feature importance analysis
8. **Business Insights**
   - Month-to-month contract customers more likely to churn
   - Electronic check payment method linked to higher churn
   - Higher monthly charges increase churn probability

## 📈 Key Results
| Model                | Accuracy | AUC   |
|---------------------|---------|-------|
| Logistic Regression  | 0.7516  | 0.8071|
| Random Forest        | 0.7672  | 0.8179|

- Top features influencing churn: `TotalCharges`, `tenure`, `MonthlyCharges`, `PaymentMethod_Electronic check`, `InternetService_Fiber optic`

## 💡 Business Insights
- Customers on **month-to-month contracts** are at higher risk  
- **Automatic payments** reduce churn compared to electronic checks  
- High monthly charges and short tenure increase churn probability  

## ✅ Conclusion
- Random Forest slightly outperformed Logistic Regression  
- SMOTE helped handle class imbalance effectively  
- Insights can guide **retention strategies** and reduce churn  

## 🚀 Next Steps
- Experiment with XGBoost/LightGBM for potentially better performance  
- Deploy a real-time churn prediction dashboard  
- Use customer segmentation for personalized offers

## 📂 Project Files
- `Telco Customer Churn-LogisticRegression.ipynb` — main notebook  
- Visualizations and output tables included in the notebook



