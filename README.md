# fraud-detection
# 💳 Fraud Detection System using Machine Learning

## 🚀 Project Overview
This project focuses on detecting fraudulent financial transactions using machine learning. The dataset contains over 6 million records, making it a large-scale real-world problem.

The objective is to classify transactions as fraudulent or non-fraudulent based on transaction details.

---

## 📁 Dataset
- Total records: **6.3 million+**
- Fraud cases: **0.13% (highly imbalanced dataset)**

### Features:
- Transaction type (TRANSFER, CASH_OUT, etc.)
- Amount
- Account balances (before & after transaction)
- Derived features (balance differences)
- Target: `isFraud`

---

## 🔍 Key Steps Performed

### 1. Data Cleaning
- Verified no missing values
- Checked class imbalance (extreme skew)

### 2. Exploratory Data Analysis (EDA)
- Fraud distribution analysis
- Transaction type vs fraud rate
- Log transformation of transaction amounts
- Time-based fraud trends

### 3. Feature Engineering
- Created new features:
  - `balanceDiffOrig`
  - `balanceDiffDest`
- Removed irrelevant columns:
  - nameOrig, nameDest
- Identified fraud-prone transaction types:
  - TRANSFER
  - CASH_OUT

---

## ⚠️ Key Insight
- Fraud occurs mostly in **TRANSFER and CASH_OUT**
- Dataset is **highly imbalanced (0.13%)**
- Many frauds happen when:
  - Old balance > 0 and new balance becomes 0

---

## 🤖 Model Building

Used a machine learning pipeline:
- StandardScaler for numeric features
- OneHotEncoder for categorical features
- Logistic Regression with class balancing

### Pipeline:
- Preprocessing + Model combined using `Pipeline` and `ColumnTransformer`

---

## 📈 Model Performance

- Accuracy: **~94.5%**
- High recall for fraud detection (important for real-world use)

### Evaluation:
- Classification Report
- Confusion Matrix

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pipeline & ColumnTransformer
- Joblib

---

## 💾 Model Deployment
# 💳 Fraud Detection System using Machine Learning

## 🚀 Project Overview
This project focuses on detecting fraudulent financial transactions using machine learning. The dataset contains over 6 million records, making it a large-scale real-world problem.

The objective is to classify transactions as fraudulent or non-fraudulent based on transaction details.

---

## 📁 Dataset
- Total records: **6.3 million+**
- Fraud cases: **0.13% (highly imbalanced dataset)**

### Features:
- Transaction type (TRANSFER, CASH_OUT, etc.)
- Amount
- Account balances (before & after transaction)
- Derived features (balance differences)
- Target: `isFraud`

---

## 🔍 Key Steps Performed

### 1. Data Cleaning
- Verified no missing values
- Checked class imbalance (extreme skew)

### 2. Exploratory Data Analysis (EDA)
- Fraud distribution analysis
- Transaction type vs fraud rate
- Log transformation of transaction amounts
- Time-based fraud trends

### 3. Feature Engineering
- Created new features:
  - `balanceDiffOrig`
  - `balanceDiffDest`
- Removed irrelevant columns:
  - nameOrig, nameDest
- Identified fraud-prone transaction types:
  - TRANSFER
  - CASH_OUT

---

## ⚠️ Key Insight
- Fraud occurs mostly in **TRANSFER and CASH_OUT**
- Dataset is **highly imbalanced (0.13%)**
- Many frauds happen when:
  - Old balance > 0 and new balance becomes 0

---

## 🤖 Model Building

Used a machine learning pipeline:
- StandardScaler for numeric features
- OneHotEncoder for categorical features
- Logistic Regression with class balancing

### Pipeline:
- Preprocessing + Model combined using `Pipeline` and `ColumnTransformer`

---

## 📈 Model Performance

- Accuracy: **~94.5%**
- High recall for fraud detection (important for real-world use)

### Evaluation:
- Classification Report
- Confusion Matrix

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pipeline & ColumnTransformer
- Joblib

---

## 💾 Model Deployment
- Saved trained pipeline using:
https://fraud-detection-f4zdrc7hczaya3cddyyx2y.streamlit.app/
- Saved trained pipeline using:
```python
joblib.dump(pipeline, "fraud_detection_pipeline.pkl")
