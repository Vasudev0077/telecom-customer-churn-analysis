# Telecom Customer Churn Analysis & Data Pipeline

## 📌 Project Overview
An end-to-end data analytics and structural preprocessing pipeline built over a 512-row customer subscription dataset. This project addresses messy real-world data patterns (mixed object-text labels, missing values, string currency characters) and engineers 7 distinct statistical visualizations using **Seaborn** and **Matplotlib** to isolate core drivers of customer attrition.

## 🛠️ Tech Stack & Skills Used
* **Languages:** Python
* **Libraries:** Pandas, NumPy, Seaborn, Matplotlib
* **Core Techniques:** 
  * Explicit data type casting (`pd.to_numeric`, `astype('int64')`)
  * Data cleaning (handling explicit case-sensitive string variations, currency symbol stripping)
  * Imputation logic (median filling for charges, analytical computation for dependent revenue features)
  * Multi-variable risk clustering & behavioral trends identification

## 📊 Core Analytical Framework & Insights

* **1. Longitudinal Spending Trajectories over Customer Lifespan**
  * *Insight:* Customer lifetime spend tracks linearly over time for both groups, but revenue volatility increases significantly after 40 months of tenure.
* **2. Categorical Churn Risk Matrix by Billing and Contract Profile**
  * *Insight:* Customers combining Month-to-Month contracts with Bank Transfers or Unknown payment profiles represent the platform's highest risk clusters, with churn rates approaching 50%.
* **3. Average Monthly Charges Across Contract Tiers and Churn Status**
  * *Insight:* High recurring monthly fees are strongly associated with cancellation behavior among short-term Month-to-Month users, whereas long-term contract users remain insensitive to price changes.
* **4. Multi-Variable Interaction: Tenure vs. Lifetime Value Growth**
  * *Insight:* Churned accounts are highly concentrated in the low-tenure, low-value quadrant, visibly mapping the strict mathematical growth path of customer acquisition economics ($TotalCharges = Tenure \times MonthlyCharges$).
* **5. Baseline Distribution of Churn (Class Imbalance Metric)**
  * *Insight:* The dataset exhibits a notable class imbalance toward retained users, indicating that predictive modeling steps will require balanced evaluation metrics (Precision, Recall, F1-Score) rather than raw accuracy scores.
* **6. Customer Retention Danger Zone Across Tenure Months**
  * *Insight:* An overlapping distribution analysis isolates a high-probability "danger zone" for customer cancellations within the first 12 months of service onboarding.
* **7. Churn Disparity Between Standard Users vs. Senior Citizens**
  * *Insight:* Senior citizens experience a significantly higher rate of subscription churn than non-seniors, highlighting a critical demographic that requires targeted retention initiatives or accessibility improvements.

## 🚀 Future Scope & Roadmap
* **Machine Learning Readiness:** The structured dataset has been fully optimized for classification pipelines. The next development phase includes one-hot encoding for historical categorical arrays (`ContractType`, `PaymentMethod`, `Gender`) and establishing a predictive model to flag high-risk accounts.
* **SQL Querying Layer (Coming Soon):** Migrating the cleaned structural dataset into a relational framework to execute structured database queries for advanced analytical business reporting, data access optimization, and cross-table cohort tracking.
