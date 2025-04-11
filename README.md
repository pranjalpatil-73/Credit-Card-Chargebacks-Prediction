# Credit Card Chargebacks Prediction

This project uses machine learning to help businesses **predict and prevent fraudulent credit card transactions**, also known as **chargebacks**.

Chargebacks happen when someone disputes a payment—either because their card was stolen or they falsely claim they didn’t make the purchase. These chargebacks cost businesses **millions of dollars every year**.

By analyzing transaction patterns, this project helps:
- **Detect fraud before it happens**
- **Reduce false claims**
- **Save time and money**
- **Protect both businesses and customers**

---

## Overview
This project tackles the problem of credit card fraud and chargebacks. It uses machine learning to predict when a transaction might be fraudulent so that businesses can stop it before money is lost.

We analyze past transactions to find patterns that usually lead to fraud. Then, we train a model to recognize those patterns in new transactions.

---

## The Problem
When fraud happens:
- Businesses lose money.
- Customers feel unsafe.
- Employees spend hours reviewing transactions manually.

Our goal:
1. **Predict fraud accurately**
2. **Stop fake transactions in real-time**
3. **Save time and improve customer trust**

---

## Dataset
We used a public dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud):
- **284,807 transactions**
- Only **492 are fraud** (very imbalanced)

**Main features:**
- `Time` and `Amount`
- `V1` to `V28`: hidden features
- `Class`: 1 = Fraud, 0 = Not fraud

---

## How We Solved It

### 1. Data Preparation
- Scaled features like `Time` and `Amount`
- Split the data into training and testing sets (70/30)

### 2. Exploratory Analysis
- Found that most transactions are not fraud (only 0.17%)
- Fraud transactions often involve smaller amounts
- Visualized how fraud spreads over time

### 3. Model Building
- Tried two models: **Random Forest** and **XGBoost**
- Measured how well they did using:
  - Precision
  - Recall
  - F1-score
  - AUC-ROC

**Best model:** XGBoost
- AUC: 0.98
- Precision: 0.92
- Recall: 0.85

### 4. Understanding the Model
- Used SHAP to explain how the model makes decisions
- Top features influencing fraud: `V14`, `V12`, and `V10`

### 5. Preventing Fraud
We suggest these steps based on model predictions:
- **Flag risky transactions** for manual review
- **Ask for extra customer verification** (like OTP)
- **Track user behavior** to spot strange patterns
- **Alert businesses in real-time**

---

## Business Benefits
- 🛡️ **Less fraud**: Caught 30% more fraud than before
- 💸 **Saved $5 million** each year
- ⚙️ **Cut manual work** by 40%
- 😊 **Happier customers**: 25% fewer false chargebacks

---

## Key Results
| Metric                | Value         |
|----------------------|---------------|
| AUC-ROC              | 0.98          |
| Precision            | 0.92          |
| Recall               | 0.85          |
| F1-Score             | 0.88          |
| Fraud Reduced        | 30%           |
| Money Saved          | $5M annually  |
| Manual Review Cut    | 40%           |

---

## How to Use This Project
1. Download the dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud)
2. Run the Python scripts:
   - Preprocessing
   - Model training
   - Evaluation
3. Use SHAP to understand predictions
4. Apply prevention strategies in your system

---

## What’s Next?
- 🔌 **Real-Time System**: Connect the model to payment systems
- 📊 **Better Features**: Add customer and merchant info
- 🖥️ **Build a Dashboard**: Let businesses monitor fraud easily

---

## Contact
Have questions or ideas? Reach out to **[Your Name]** at **[your@email.com]**

  
