# Customer Churn Prediction with Logistic Regression

**Duration:** June 7-8 2025
  
**Tools Used:** Python, Pandas, Seaborn, Scikit-learn, Matplotlib  

## Overview

This project analyzes customer churn behavior using the Telco Customer Churn dataset. The goal is to build a logistic regression model to predict whether a customer is likely to churn based on their demographic and service usage attributes.

---

## Steps Performed

### 1. Data Loading & Cleaning
- Loaded the Telco churn dataset using Pandas.
- Dropped the `customerID` column and handled missing values in `TotalCharges` by converting to numeric and dropping nulls.

### 2. Exploratory Data Analysis (EDA)
- Visualized the churn distribution using `sns.countplot`.
- Noted class imbalance with more customers not churning.

![Churn Distribution](churn_distribution.png)

### 3. Feature Engineering
- Converted categorical variables to numerical using one-hot encoding (`pd.get_dummies`).
- Dropped one category per feature to avoid multicollinearity.

### 4. Model Development
- Defined features (`X`) and target (`y`), where churned customers were encoded as `1`.
- Split data into training and testing sets (80/20 split).
- Trained a logistic regression model with `max_iter=600`.

### 5. Model Evaluation
- Evaluated using accuracy, confusion matrix, and classification report.
- Accuracy score printed to assess overall performance.

![Confusion Matrix](confusion_matrix.png)

### 6. Feature Importance
- Extracted and plotted top positive coefficients from the logistic regression model.
- Identified key features contributing to churn risk (e.g., contract type, tenure, monthly charges).

![Top Positive Features Influencing Churn](top_positive_features_influencing_hurn.png)

---

## Outcomes

- Built a baseline churn classification model using logistic regression.
- Achieved interpretable results highlighting key churn indicators.
- Gained insights into which service factors are most correlated with customer attrition.

---

## Next Steps

- Experiment with advanced models (Random Forest, XGBoost).
- Address class imbalance using SMOTE or class weights.
- Deploy the model using Flask or Streamlit for business use.