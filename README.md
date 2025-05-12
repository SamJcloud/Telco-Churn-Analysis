# Telco Customer Churn Analysis

This project investigates customer churn behavior at a telecom company using the popular Telco Customer Churn dataset. It involves SQL-based data exploration, data preprocessing in Python, and modeling with Logistic Regression — all focused on drawing meaningful, explainable insights rather than deploying a model.

---

## 🔍 Project Objectives

- Import and explore a relational dataset using SQLite and SQL queries
- Perform data cleaning and preprocessing in Python
- Apply Logistic Regression to predict churn
- Extract and interpret feature importances
- Generate actionable business insights from model results

---

## 📊 Dataset

**Source**: IBM Sample Dataset (Telco Customer Churn)  
**Records**: ~7,000  
**Target**: `Churn` (Yes/No)  
**Features**: Customer demographics, services subscribed, billing info, etc.

---

## 🛠️ Tools & Libraries

- **SQL (SQLite)** – for raw data exploration
- **Pandas / NumPy** – for data manipulation
- **Scikit-learn** – preprocessing, modeling, and evaluation
- **Matplotlib / Seaborn** – data visualization


---

## 🔁 Workflow

### 1. Data Ingestion
- Dataset loaded and queried using SQLite
- Joined customer, service, and billing data for rich feature set

### 2. Data Preprocessing
- Imputation: `SimpleImputer` for missing values
- Scaling: `StandardScaler` for numerical features
- Encoding: `OneHotEncoder` with `drop='first'` to avoid multicollinearity
- Final preprocessing pipeline: `ColumnTransformer`

### 3. Modeling
- **Primary Model**: Logistic Regression (`scikit-learn`)
- Train-Test Split: 80/20 with stratification
- Evaluation Metrics: Accuracy

### 4. Feature Importance & Interpretation
- Extracted coefficients from Logistic Regression
- Identified top features driving churn and retention
- Visualized with bar plots for explainability

---

## ✅ Results

### Logistic Regression
- **Training Accuracy**: ~0.80  
- **Test Accuracy**: ~0.81  


### Feature Insights

| Feature                        | Effect on Churn         |
|-------------------------------|--------------------------|
| `Contract_Two year`           | Strongly reduces churn   |
| `tenure`                      | Longer tenure = retention|
| `InternetService_Fiber optic`| Increases churn risk     |
| `PaymentMethod_Electronic`   | Increases churn risk     |
| `MonthlyCharges`             | Higher cost = more churn |

---

## 📌 Key Business Insights

- **Retention Strategy**: Customers on longer-term contracts and with higher tenure are less likely to churn.
- **Risk Segments**: Fiber-optic and high monthly charge customers are at higher risk and may benefit from loyalty perks or proactive engagement.
- **Payment Behavior**: Users paying via electronic checks exhibit higher churn; investigate underlying causes.

---


---

## ✍️ Author

**SamJ** – Chemical Engineer & Data Analytics Enthusiast  
Learning to bridge data engineering, analytics, and ML for impactful decision-making.



