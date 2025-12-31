# Adey Innovations: Real-Time Fraud Detection System

## 📌 Project Overview
Adey Innovations is a leading fintech company. This project focuses on building a robust Machine Learning pipeline to detect fraudulent transactions. The system analyzes user behavioral patterns—such as the time between signup and purchase—and device metadata to separate legitimate customers from sophisticated fraud rings.

## 🛠️ Key Features
- **Class Imbalance Handling:** Implementation of SMOTE to address the 1:99 fraud-to-legit ratio.
- **Feature Engineering:** Creation of behavioral metrics including `time_diff` and device/IP frequency tracking.
- **Model Comparison:** Rigorous testing between Logistic Regression and Random Forest ensembles.
- **Explainable AI (XAI):** Integration of SHAP values to provide "Glass-Box" transparency for automated decisions.

## 📂 Project Structure
```text
├── data/
│   ├── raw/                # Original datasets (Fraud_Data.csv, ip_address.csv, creditcard.csv)
│   └── processed/          # Scaled, encoded, and SMOTE-balanced datasets
├── models/
│   └── fraud_rf_model.pkl  # Final trained Random Forest model
├── notebooks/
│   ├── 01_EDA_Preprocessing.ipynb  # Data cleaning, visualization, and engineering
│   ├── 02_Model_Training.ipynb     # Model selection and hyperparameter tuning
│   └── 03_Interpretability.ipynb    # SHAP analysis and feature importance
├── reports/
│   └── Final_Project_Report.pdf    # Comprehensive narrative of findings
├── requirements.txt                # Python dependencies
└── README.md                       # Project documentation

## ⚙️ Setup Instructions
1. Clone the repository: `git clone [https://github.com/Aperca/Fraud_Detection.git]`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebooks in order: `01 -> 02 -> 03`

## Results Summary
1. Primary Model: Random Forest Classifier

2. Precision: 0.92 (92% of flagged transactions are confirmed fraud)

3. Top Predictor: time_diff (Sign-up to Purchase latency)