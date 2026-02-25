# Customer Churn Analysis: Telco Industry

🇧🇷 [Clique aqui para a versão em Português](README_PTBR.md)

## 📌 Project Overview
This project aims to predict customer attrition (churn) for a telecommunications company. By identifying at-risk customers, the business can proactively offer incentives to improve retention and protect monthly revenue.



## 📊 The Data
The dataset consists of **7,043 customers** with 21 features, including:
* **Demographics:** Gender, senior citizenship, partners, and dependents.
* **Services:** Phone, internet (Fiber optic/DSL), tech support, etc.
* **Account Info:** Tenure, contract type, and payment method.

## 🛠️ Technical Workflow
1. **Data Cleaning:** Handled missing values in `TotalCharges` and used **One-Hot Encoding** for categorical variables.
2. **EDA:** Discovered that customers with **Month-to-Month contracts** and **Fiber Optic** internet have the highest churn rates.
3. **Modeling:** Compared **Logistic Regression** vs. **Random Forest** using default hyperparameters to establish a baseline.

## 📈 Performance Comparison

| Model | AUC Score | Key Takeaway |
| :--- | :---: | :--- |
| **Logistic Regression** | **0.84** | Best overall performance and highly interpretable. |
| **Random Forest** | **0.82** | Strong performance; useful for non-linear patterns. |



## 💡 Business Insights
* **High-Risk Contracts:** Month-to-month plans are churn drivers.
* **Critical Period:** New customers (first 6 months) require more attention.
* **Upselling Opportunity:** Customers without Tech Support churn more frequently.
