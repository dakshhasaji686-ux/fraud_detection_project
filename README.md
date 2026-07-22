# Credit Card Fraud Detection using Machine Learning

# presentation of this project
  https://drive.google.com/file/d/1XAQHq4tfqnuWvrlXAJdf5CZZePFFBhGF/view?usp=drive_link

## 📌 Project Overview

This project aims to detect fraudulent credit card transactions using supervised machine learning algorithms. Since fraud transactions are extremely rare compared to legitimate ones, the project focuses on handling class imbalance using multiple techniques and selecting the best-performing model through proper evaluation metrics.

The complete machine learning pipeline includes data preprocessing, exploratory data analysis (EDA), feature engineering, class imbalance handling, model training, hyperparameter tuning, threshold optimization, business cost analysis, and model deployment.

---

## 🎯 Objectives

- Detect fraudulent credit card transactions accurately.
- Handle highly imbalanced datasets.
- Compare multiple supervised learning algorithms.
- Optimize model performance using hyperparameter tuning.
- Find the optimal classification threshold.
- Perform business cost-benefit analysis.
- Save the best model for deployment.

---

## 📂 Dataset

**Dataset Name:** Credit Card Fraud Detection

**Source:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

### Features

- Time
- Amount
- V1–V28 (PCA-transformed features)
- Class (Target)

### Target Variable

- **0** → Legitimate Transaction
- **1** → Fraudulent Transaction

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost
- Joblib
- Jupyter Notebook

---

# 📊 Project Workflow

```
Load Dataset
      │
      ▼
Data Inspection
      │
      ▼
Data Preprocessing
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Engineering
      │
      ▼
Handle Class Imbalance
      │
      ▼
Model Building
      │
      ▼
Hyperparameter Tuning
      │
      ▼
Threshold Optimization
      │
      ▼
Business Cost Analysis
      │
      ▼
Model Saving
```

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Checked missing values
- Removed duplicate records
- Performed stratified sampling (50,000 records)
- Created new features:
  - Amount_log
  - Hour
- Applied StandardScaler
- Split dataset into training and testing sets

---

# 📈 Exploratory Data Analysis

EDA included:

- Class Distribution
- Transaction Amount Distribution
- Transaction Time Distribution
- Boxplots
- Correlation Heatmap

---

# ⚖️ Handling Class Imbalance

Three approaches were compared:

- Original Dataset
- SMOTE Oversampling
- Random Under Sampling

---

# 🤖 Machine Learning Models

The following models were implemented:

### Logistic Regression

- Baseline classifier
- Used class_weight='balanced'

### Random Forest

- Ensemble learning algorithm
- Feature importance analysis

### XGBoost

- Gradient Boosting algorithm
- Used scale_pos_weight
- Hyperparameter tuning using RandomizedSearchCV

---

# 📏 Model Evaluation Metrics

Models were evaluated using:

- Precision
- Recall
- F1-Score
- PR-AUC
- Confusion Matrix
- Precision-Recall Curve

---

# 🎯 Threshold Optimization

Instead of using the default threshold (0.5), the project identifies:

- Best F1 Threshold
- Threshold achieving Recall ≥ 90%

This allows the model to better align with business requirements.

---

# 💼 Business Cost Analysis

A business simulation was performed using the following assumptions:

- ₹4500 saved for every fraud detected
- ₹150 investigation cost for each flagged transaction

Calculated metrics:

- Money Saved
- Investigation Cost
- Money Lost
- Net Benefit

The threshold with the highest Net Benefit was selected for deployment.

---

# 📁 Project Structure

```
CreditCardFraudDetection/

│── creditcard.csv
│── FraudDetection.ipynb
│── fraud_detection_model.pkl
│── requirements.txt
│── README.md
│── summary_report.md
```

---

# 👨‍💻 Author

**Daksh Hasaji**


