# 💳 Credit Risk Prediction Model

## 📌 Project Overview

This project focuses on building a **Credit Risk Prediction Model** to identify whether a customer is likely to default on a loan. The workflow includes **data cleaning, feature engineering, and machine learning modeling** using real-world-inspired credit data.

The goal is to help financial institutions make **data-driven lending decisions** by assessing risk efficiently.

---

## ⚙️ Project Structure

```
App/
│
├── credit model.ipynb                # Data cleaning & preprocessing
├── credit model version 2.ipynb     # Feature engineering
├── credit model version 3.ipynb     # Model training & evaluation
│
├── data/
│   ├── credit_data_realistic_v2_dirty.csv
│   ├── data_processed_credit_data_cleaned_v2.csv
│   ├── data_processed_credit_data_features_v2.csv
```

---

## 🔄 Workflow

### 1. Data Cleaning & Exploration

* Load raw dataset
* Handle missing values
* Identify invalid entries
* Generate data profile:

  * Data types
  * Missing percentage
  * Unique values
* Perform statistical analysis

---

### 2. Feature Engineering

New features are created to improve model performance:

* **Debt to Income Ratio**

  ```
  debt_to_income = loan_amount / annual_income
  ```
* **Utilization Stress**

  ```
  utilization_stress = credit_utilization²
  ```
* **Exposure Ratio**

  ```
  exposure_ratio = loan_amount / credit_limit
  ```
* **Average Payment Delay**

  ```
  avg_payment_delay = mean(pay_delay_m1 ... pay_delay_m6)
  ```

✔️ Outliers are controlled using clipping.

---

### 3. Model Building

* Algorithm used: **Logistic Regression**
* Train-test split applied
* Feature scaling using **StandardScaler**

---

## 📊 Evaluation Metrics

The model is evaluated using:

* **ROC-AUC Score**
* **Confusion Matrix**
* **Classification Report**

  * Precision
  * Recall
  * F1-score

---

## 🧠 Key Features Used

* debt_to_income
* utilization_stress
* exposure_ratio
* avg_payment_delay
* (other engineered financial indicators)

---

## 🚀 How to Run

### Step 1: Install Dependencies

```bash
pip install pandas numpy scikit-learn
```

### Step 2: Run Notebooks

1. Run `credit model.ipynb` → Data cleaning
2. Run `credit model version 2.ipynb` → Feature engineering
3. Run `credit model version 3.ipynb` → Model training

---

## 📈 Future Improvements

* Try advanced models (Random Forest, XGBoost)
* Hyperparameter tuning
* Add more behavioral features
* Deploy as a web app (Flask / Streamlit)

---

## 🎯 Use Cases

* Loan approval systems
* Banking risk assessment
* Fintech credit scoring

---

## 👨‍💻 Author

**Sairanjan Choudhury**
AI & ML Engineering Student

---

## 📌 Notes

* This is a **learning + portfolio project**
* Dataset is realistic but may be synthetic or modified for practice

---

⭐ If you found this useful, consider improving it with advanced ML models!
