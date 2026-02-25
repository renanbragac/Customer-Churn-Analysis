# Customer Churn Analysis: Telco Industry

🇧🇷 [Clique aqui para a versão em Português](README.md)

## 📌 Project Overview
This project predicts customer attrition (churn) for a telecommunications company. Identifying at-risk customers allows for proactive retention strategies to minimize revenue loss.



## 📊 The Data
The dataset includes **7,043 customers** with features such as demographics, subscribed services, and account information (tenure, contract type).

## 🛠️ Technical Workflow
1. **Data Prep:** Cleaned missing values and applied **One-Hot Encoding**.
2. **EDA:** Discovered that **Month-to-Month** contracts and **Fiber Optic** internet are top churn drivers.
3. **Modeling:** Compared **Logistic Regression** and **Random Forest** baselines.

## 📈 Performance Comparison

| Model | AUC Score | Key Takeaway |
| :--- | :---: | :--- |
| **Logistic Regression** | **0.84** | Higher accuracy and easy to interpret for stakeholders. |
| **Random Forest** | **0.82** | Captures complex, non-linear relationships. |

## 💡 Business Insights
* **Retention:** Transition monthly customers to long-term contracts.
* **Engagement:** Prioritize engagement during the first 6 months (critical tenure).
* **Service Bundling:** Promote Tech Support services to reduce churn probability.
