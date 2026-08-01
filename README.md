# 💳 CreditWise Loan Approval Prediction System

An end-to-end Machine Learning project that predicts whether a loan application should be **Approved** or **Rejected** based on an applicant's financial, demographic, and credit-related information.

The goal is to assist financial institutions in making faster, consistent, and data-driven lending decisions.

---

## 📌 Problem Statement

SecureTrust Bank, a mid-sized financial company operating across urban and rural India, currently relies on **manual verification** of applicant documents — checking income proofs, employment details, and credit history by hand. This makes the process:

- Time-consuming
- Prone to human bias
- Inconsistent across applications

As a result, good customers sometimes get rejected (lost business), and high-risk customers sometimes get approved (financial loss).

This project leverages historical loan application data to build a predictive machine learning model capable of identifying applicants with a high probability of loan approval.

---

## 🎯 Objectives

- Perform comprehensive Exploratory Data Analysis (EDA)
- Clean and preprocess the dataset
- Handle missing values and categorical variables
- Engineer useful features
- Train Machine Learning classification models
- Evaluate and compare model performance
- Generate business insights

---

## 📂 Dataset

1,000 applicant records with the following features:

- Applicant Income
- Co-applicant Income
- Employment Status
- Age
- Marital Status
- Dependents
- Credit Score
- Existing Loans
- Debt-to-Income Ratio
- Savings
- Collateral Value
- Loan Amount
- Loan Term
- Loan Purpose
- Property Area
- Education Level
- Gender
- Employer Category

**Target Variable:** `Loan_Approved`
- 1 → Approved
- 0 → Rejected

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

## 📊 Workflow

1. Data Loading
2. Missing Value Treatment (mean imputation for numerical, most-frequent for categorical)
3. Exploratory Data Analysis
4. Outlier Detection (boxplots)
5. Encoding Categorical Variables (Label Encoding + One-Hot Encoding)
6. Correlation Analysis
7. Train-Test Split
8. Feature Scaling (StandardScaler)
9. Model Training
10. Model Evaluation
11. Feature Engineering (polynomial features)
12. Re-evaluation & Model Selection

---

## 📈 Exploratory Data Analysis

Key analyses performed:

- Loan Approval Class Distribution
- Education Level Distribution
- Applicant & Co-applicant Income Distribution
- Income vs Loan Approval (Boxplots)
- Credit Score vs Loan Approval
- DTI Ratio & Savings vs Loan Approval
- Correlation Heatmap across all numerical features

---

## 🤖 Machine Learning

Three classification models were trained and compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes (GaussianNB)

**Evaluation metrics used:**
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Results (after Feature Engineering)

| Model | Precision | Recall | F1-Score | Accuracy |
|---|---|---|---|---|
| **Logistic Regression** ✅ | 0.785 | 0.836 | **0.810** | **0.88** |
| Naive Bayes | 0.811 | 0.705 | 0.754 | 0.86 |
| KNN (k=5) | 0.673 | 0.574 | 0.619 | 0.785 |

**Logistic Regression** was selected as the best-performing model, achieving the highest accuracy (88%) and F1-score (0.810) after adding engineered features (`DTI_Ratio²`, `Credit_Score²`).

---

## 💡 Business Insights

- Credit Score and DTI Ratio showed the strongest correlation with loan approval outcomes
- Applicants with higher savings and lower existing loans had noticeably higher approval rates
- Linear models outperformed distance-based models (KNN) on this dataset, suggesting the decision boundary between approved/rejected applicants is largely linear
- Feature engineering (squared terms) improved model discrimination without needing complex non-linear models

---

## 📁 Project Structure

CreditWise-Loan-Approval-Prediction/
│
├── credit_wise.ipynb
├── loan_approval_data.csv
├── CreditWise_Loan_System.pdf
├── README.md
├── LICENSE
└── requirements.txt

---

## 🚀 Installation

git clone https://github.com/ArchitJain-13/CreditWise-Loan-Approval-Prediction.git
cd CreditWise-Loan-Approval-Prediction
pip install -r requirements.txt

---
## ▶️ Run

Open Jupyter Notebook:
jupyter notebook

Then open:
credit_wise.ipynb
---

## 📌 Future Improvements

- Hyperparameter Tuning (GridSearchCV)
- XGBoost / LightGBM / Random Forest
- Explainable AI using SHAP
- Handle class imbalance with SMOTE
- Flask/FastAPI Deployment
- Streamlit Dashboard
- Docker Support

---

## 📜 License

This project is developed for educational and portfolio purposes.

---

## 👨‍💻 Author

**Archit Jain**
B.Tech Computer Science & Systems Engineering (KIIT University)
Machine Learning | Backend Development | AI

GitHub: [ArchitJain-13](https://github.com/ArchitJain-13)
