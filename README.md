# Hypothesis-Driven Analysis of Credit Card Customer Data

This project applies statistical and machine learning methods to analyze a real-world credit card customer dataset. The goal is to test two business-critical hypotheses related to **credit limit determination** and **customer attrition risk** — helping financial institutions make better data-driven decisions.

📄 Report: [LINK](https://github.com/shreyasah99/Hypothesis-Driven-Analysis-on-Credit-Limits-and-Attrition/blob/main/final%20project%20report.pdf)  
📊 Presentation: [LINK](https://github.com/shreyasah99/Hypothesis-Driven-Analysis-on-Credit-Limits-and-Attrition/blob/main/Ppt%20PDF.pdf)


---

## 📌 Table of Contents
- [Introduction](#introduction)
- [What We Did](#what-we-did)
- [Dataset Overview](#dataset-overview)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Hypothesis 1: Gender and High Credit Limit](#hypothesis-1-gender-and-high-credit-limit)
- [Hypothesis 2: Utilization Ratio and Customer Attrition](#hypothesis-2-utilization-ratio-and-customer-attrition)
- [Results and Insights](#results-and-insights)
- [Business Recommendations](#business-recommendations)
- [Limitations and Future Work](#limitations-and-future-work)
- [Team](#team)

---

## 🧠 Introduction

Credit cards play a pivotal role in today’s financial systems. Understanding the behaviors and attributes of credit card users can help financial institutions with strategic planning, customer satisfaction, and profitability.

This project analyzes credit card customer information to uncover insights using **hypothesis testing** and **logistic regression modeling**.

---

## 🛠️ What We Did

- Cleaned and preprocessed a credit card customer dataset
- Conducted Exploratory Data Analysis (EDA)
- Formulated and tested two business hypotheses
- Used statistical tests: **Z-Test**, **Chi-Square Test**, and **Logistic Regression**
- Derived strategic insights and actionable recommendations

---

## 📂 Dataset Overview

- Contains customer-level demographic and financial data from 2018–2019.
- Features include:
  - `Credit_Limit`
  - `Attrition_Flag`
  - `Avg_Utilization_Ratio`
  - `Education_Level`, `Income_Category`, `Gender`, etc.

---

## 📊 Exploratory Data Analysis (EDA)

- Identified outliers in credit limits and removed them to reduce skew.
- Analyzed distributions of key variables like `Credit_Limit`, `Customer_Age`, and `Utilization_Ratio`.
- Investigated relationships between gender, income, education, and credit limits.

---

## 🧪 Hypothesis 1: Gender and High Credit Limit

**Hypothesis Statement:**

> Is the percentage of males among customers with credit limits > $25,000 significantly more than 90%?

**Tests Used:**
- One-sample **Z-Test** for proportions
- **Chi-Square Test** for association between `Gender` and `Credit_Limit`

**Result:**
- **Z-Test:** Fail to reject null; proportion ≈ 90.4%
- **Chi-Square Test:** No significant relationship between `Gender` and `Credit_Limit`
- Instead, **Income** and **Education Level** were found to be stronger predictors of high credit limits.

---

## 🧪 Hypothesis 2: Utilization Ratio and Customer Attrition

**Hypothesis Statement:**

> Do customers with utilization ratios below 0.5 have a higher likelihood of attrition?

**Test Used:**
- **Logistic Regression** modeling
- Supported by **Chi-Square Test** on categorical variable `utilization_less_than_0.5`

**Result:**
- Logistic regression showed a **highly significant relationship**
  - p-value ≈ **1.14e-12**
  - Customers with `utilization < 0.5` are more likely to **attrite**
- Chi-Square test validated the result

---

## 💡 Results and Insights

- **Gender is not a strong predictor** of credit limits; **education and income** are more influential.
- **Utilization ratio is a key indicator** of customer attrition — customers who underutilize their credit lines are more likely to leave.
- Hypothesis testing and modeling revealed actionable customer segments for retention and engagement strategies.

---

## 💼 Business Recommendations

1. **Targeted Retention Campaigns**  
   Engage customers with low utilization ratios through personalized offers or communication.

2. **Customized Credit Offers**  
   Base credit limit decisions more on education and income than demographic features like gender.

3. **Utilization Education Programs**  
   Educate users on benefits of optimal utilization to reduce attrition risk.

4. **Monitoring & Alerts**  
   Implement systems to monitor usage patterns and flag high-risk customers early.

---

## ⚠️ Limitations and Future Work

- Dataset covers only a static time frame (2018–2019); trends may change.
- Causal relationships are not confirmed — only statistical correlations.
- Future improvements:
  - Add longitudinal data
  - Use external financial indicators
  - Try advanced ML models like Random Forest or XGBoost

---

## 👥 Team

- Nayan Bhiwapurkar  
- Kaumudi Patil  
- Shreyas Hingmire  
- Sharan Patel  

---

## 📎 References

- UCI & Kaggle credit card datasets
- Statsmodels & Scipy for hypothesis testing
- Logistic Regression using `statsmodels.api.Logit`

---

> Feel free to clone this repo, try the notebooks, or extend our analysis using new models or datasets!
