# Loan Default Prediction: Data Analysis & Machine Learning Model

## 📌Project Overview
Loan default prediction is a crucial aspect of risk management for financial institutions. This project aims to analyze loan data, identify key factors influencing loan defaults, and develop a predictive model to help lenders make data-driven lending decisions.

The project consists of **two main stages**:
1. **Data Analysis Preprocessing:** Cleaning and exploring the dataset to uncover insights.
2. **Predictive Modeling:** Building a logistic regression model to classify loan applicants as either likely to default or not.

---

## 📂Dataset Description
The dataset consists of historical loan records with the following key features:

| Column Name           | Description |
|-----------------------|-------------|
| `id`                 | Unique loan ID |
| `issue_d`            | Loan issue date |
| `loan_amnt`          | Amount of the loan requested |
| `loan_status`        | Target variable (1: Non-default, 0: Default) |
| `funded_amnt`        | Amount funded by investors |
| `term`               | Loan repayment period (e.g., 36 months, 60 months) |
| `int_rate`           | Interest rate of the loan (%) |
| `installment`        | Monthly payment amount |
| `grade`              | Credit rating assigned to the loan |
| `sub_grade`          | More granular credit rating |
| `verification_status` | Whether the borrower's information was verified |
| `addr_state`         | State of residence of the borrower |
| `total_pymnt`        | Total amount paid by the borrower |

---

## 🔎Data Analysis & Preprocessing
Before building a predictive model, **intensive data cleaning and preprocessing** were performed:
- **Handling Missing Values:** Dropped or imputed missing values.
- **Feature Engineering:** Derived meaningful features from existing columns.

---

## 🤖Modeling Approach
A **logistic regression model** was used for prediction. However, due to class imbalance:
1. **Baseline Model:** The initial model predicted only the majority class (Non-default).
2. **Balanced Model:** Applied `class_weight='balanced'` in logistic regression to improve minority class recall.

---

## 📊 Results & Key Findings
- **Class Imbalance Issue:**  
  - 1.0 (Non-default): **9,428 loans**  
  - 0.0 (Default): **572 loans**  
- **Baseline Model Performance:**  
  - Predicted only **non-default** cases.
  - **Confusion Matrix:**  
    ```
    [[   0  106]
     [   0 1894]]
    ```
  - Model failed to identify any defaulters.

- **Balanced Model Performance:**  
  - Adjusting class weights improved recall for defaults but decreased accuracy.  
  - **Confusion Matrix:**  
    ```
    [[  79   27]
     [1085  809]]
    ```
  - **Accuracy:** 44%  
  - **Precision-Recall Tradeoff:** Improved recall for defaults but with lower precision.

---

## 🚀Challenges & Limitations
- **High Class Imbalance:** The dataset is biased toward non-defaulters, affecting model learning.
- **Limited Features:** Important financial indicators like income, credit history, and employment status were missing.
- **Logistic Regression Simplicity:** More advanced models might capture complex patterns better.

---

## 💡Recommendations for Improvement
1. **Apply Data Resampling:**  
   - Use **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic samples for the minority class.  
   - Try **undersampling** the majority class.  

2. **Explore Advanced Models:**  
   - Implement **Random Forest, XGBoost, or Gradient Boosting** for improved performance.  
   - Experiment with **ensemble learning**.  

3. **Feature Engineering:**  
   - Add **borrower income, credit history, and debt-to-income ratio**.  
   - Compute **loan-to-income ratio and late payment history**.  

4. **Optimize Model Thresholds:**  
   - Instead of using a default **0.5 probability cutoff**, adjust it to minimize false negatives.  

5. **Business Strategy Adjustments:**  
   - Financial institutions should **tighten lending criteria** for high-risk applicants.  
   - Consider **alternative credit scoring methods** such as transaction behavior or social media insights.  

---

## 📌Next Steps
- Implement **SMOTE or cost-sensitive learning** to further handle class imbalance.
- Try **tree-based models** like **Random Forest or XGBoost**.
- Tune hyperparameters and **deploy the best model** in a production environment.

---

## 🎯 **Conclusion**
This project highlights the **importance of handling imbalanced data in financial modeling**. While logistic regression provided some insights, **more robust techniques** are required to build a reliable loan default prediction model. Future work should focus on **feature engineering, model selection, and business implications** to make this model viable for real-world applications.

---

## 💻 Author
**David Omokhagbo Shegun**  
📧 davshegs@gmail.com  
📍 Abuja, Nigeria  

---

**🔗 Feel free to contribute, raise issues, or suggest improvements!**

