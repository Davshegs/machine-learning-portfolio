# Customer Churn Prediction Using Logistic Regression

## Project Overview  
Customer churn is a major concern for banks and financial institutions, as losing customers directly impacts revenue and business growth. This project aims to build a **Machine Learning model using Logistic Regression** to predict whether a customer will churn (leave the bank) based on various demographic and financial factors.  

By identifying customers at risk of leaving, banks can implement strategies to improve customer retention and engagement.  

---

## Dataset Description  
The dataset contains customer information with the following features:  

| Feature            | Description |
|--------------------|-------------|
| **CustomerID**     | Unique identifier for each customer (not used in modeling) |
| **Sex**           | Gender of the customer (Male/Female) |
| **Age**           | Age of the customer |
| **Geography**     | Country of the customer (France, Germany, Spain) |
| **CreditScore**   | Credit score of the customer |
| **NumOfProducts** | Number of products the customer has with the bank |
| **HasCreditCard** | Whether the customer owns a credit card (1 = Yes, 0 = No) |
| **IsActiveMember**| Whether the customer is an active bank member (1 = Yes, 0 = No) |
| **Balance**       | Account balance of the customer |
| **EstimatedSalary** | Estimated salary of the customer |
| **Exited (Target Variable)** | Whether the customer churned (1 = Yes, 0 = No) |

---

## Project Workflow  
This project follows a structured approach:  

### 1. Data Preprocessing & Exploration  
- Load the dataset and understand its structure.  
- Handle missing values (if any) and clean the data.  
- Perform exploratory data analysis (EDA) using visualizations to identify patterns and relationships affecting churn.  
- Encode categorical variables (e.g., Gender, Geography).  
- Scale numerical features for better model performance.  

### 2. Model Development  
- Split the dataset into **training (80%)** and **testing (20%)** sets.  
- Train a **Logistic Regression** model to classify customers as churned (1) or not (0).  
- Evaluate the model using **accuracy, precision, recall, and F1-score**.  

### 3. Insights & Findings  
- Identify key factors influencing customer churn.  
- Understand which customer groups are more likely to leave.  
- Provide business recommendations based on findings.  

---

## Installation & Setup  
To run this project, follow these steps:  

### 1. Clone the Repository  
```bash
git clone https://github.com/Davshegs/machine-learning-portfolio.git
cd customer-churn-prediction
```
### 2. Install Dependencies
Ensure you have Python installed, then install the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
### 3. Run the Jupyter Notebook
```bash
jupyter notebook
```
Open the customer_churn.ipynb file and execute the cells step by step.

---

## Contributors
David Omokhagbo Shegun – Data Scientist & Machine Learning Engineer
Feel free to reach out via [Email](davshegs@gmail.com) or [LinkedIn](www.linkedin.com/in/david-shegun-6a42aa29b).



