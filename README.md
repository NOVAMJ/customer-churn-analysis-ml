# 📉 Customer Churn Prediction & Analysis

Predicting customer churn for subscription-based businesses using data-driven insights and machine learning models.  
This project focuses on identifying churn risk factors, explaining model predictions, and helping businesses design retention strategies.

---

## 📌 Table of Contents
- [Overview](#overview)    
- [Dataset](#dataset)  
- [Tools & Technologies](#tools--technologies)  
- [Project Structure](#project-structure)  
- [Data Cleaning & Preparation](#data-cleaning--preparation)  
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- [Modeling](#modeling)  
- [Key Findings](#key-findings)  
- [How to Run](#how-to-run)  

---

##  Overview
Customer churn is a critical business metric. This project explores historical customer data to:  
- Predict churn using ML classification models  
- Identify key churn factors  
- Provide actionable recommendations for retention

---

##  Dataset
- **Source:** [Telco Customer Churn Dataset](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Records:** ~7,000 customer entries  
- **Features:**  
  - Demographics (gender, senior citizen, partner)  
  - Subscription details (contract type, tenure, monthly charges)  
  - Services used (internet, streaming, phone)  
  - Target: `Churn (Yes/No)`  

---

##  Tools & Technologies
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SHAP  
- **IDE:** Jupyter Notebook  
- **Version Control:** GitHub  

---

##  Project Structure
churn-prediction/
├── data/ # Raw and processed data
├── requirements.txt # Dependencies
├── notebooks/ # EDA and modeling notebooks
└── README.md # Documentation

---

##  Data Cleaning & Preparation
- Handled missing values in `TotalCharges`  
- Encoded categorical features  
- Normalized numerical variables  
- Created tenure-based customer segments

---

##  Exploratory Data Analysis (EDA)
- Higher churn observed among customers with:  
  - Month-to-month contracts  
  - High monthly charges  
  - No tech support/online security services  
- Tenure and contract type strongly influence churn risk

---

##  Modeling
- Models tested: Logistic Regression, Random Forest, k-nearest neighbors, Support Vector Machine, XGBoost and Gradient Boosting
- Best Model: **Gradient Boosting** (~86% accuracy)  
- SHAP used for feature importance and explainability  

---

##  Key Findings & Result
- **Top churn drivers:**  
  - Contract type (Month-to-Month)  
  - High monthly charges  
  - Low tenure customers  
- Customers with longer contracts churn less  
- Bundled service offers can help reduce churn

##  Result

| Model                     | Accuracy  | Recall Score | F1 Score  | ROC AUC Score |
|---------------------------|-----------|-------------|-----------|---------------|
| Logistic Regression       | 0.703667  | 0.683219    | 0.473029  | 0.764076      |
| Random Forest             | 0.862000  | 0.414384    | 0.538976  | 0.852447      |
| K-Nearest Neighbors       | 0.752333  | 0.667808    | 0.512147  | 0.776639      |
| Support Vector Machine    | 0.785667  | 0.662671    | 0.546224  | 0.822503      |
| XGBoost                   | 0.833000  | 0.609589    | 0.586974  | 0.841784      |
| Gradient Boosting         | 0.817000  | 0.700342    | 0.598391  | 0.859767      |

---

##  How to Run
```bash
# Clone repo
git clone https://github.com/username/churn-prediction.git
cd churn-prediction

# Install dependencies
pip install -r requirements.txt

# Open Jupyter Notebook
jupyter notebook notebooks/churn_analysis.ipynb
