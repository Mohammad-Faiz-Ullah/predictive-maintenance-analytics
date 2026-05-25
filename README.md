# 🔧 Predictive Maintenance Analytics & Failure Prediction

## 📌 Project Overview
This project focuses on predictive maintenance analytics using industrial machine sensor data. The workflow combines data analytics, business intelligence, and machine learning to identify machine failure patterns and support proactive maintenance decisions.

---

# 🎯 Objectives
- Analyze machine operational behavior
- Identify failure patterns and high-risk conditions
- Build business-oriented maintenance insights
- Predict machine failure using machine learning
- Create interactive analytical dashboards

---

# ⚙️ Workflow
- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Failure Pattern Analysis
- Feature Engineering
- SQL Analytics
- Power BI Dashboarding
- Logistic Regression Model Training
- Model Evaluation

---

# 📊 Exploratory Data Analysis

### Performed:
- Univariate & Multivariate Analysis
- Correlation Analysis
- Outlier Detection
- Class Imbalance Analysis
- Sensor Threshold Analysis
- Failure Pattern Visualization

### 🔍 Key Findings
- High torque and tool wear strongly influence machine failures
- Failure probability increases under operational stress
- Dataset is highly imbalanced

---

# 🛠️ Feature Engineering

### Created Additional Features
- `power`
- `temp_diff`

### Applied
- normalization
- feature transformation

---

# 🗄️ SQL Analytics

SQL was used for:
- Failure rate analysis
- Product-wise failure analysis
- KPI extraction
- High-risk machine identification

### 💻 Sample SQL Query

```sql
SELECT `Type`, COUNT(*) AS failures
FROM predictive_maintenance
WHERE `Machine failure` = 1
GROUP BY `Type`;
```

---

# 📈 Power BI Dashboard

Interactive Power BI dashboard created for:
- KPI monitoring
- Failure trend analysis
- Product-wise failure insights
- Torque and wear analysis
- Machine risk visualization

<img width="1377" height="771" alt="Milling_machine_dashboard1" src="https://github.com/user-attachments/assets/1b5fb844-0d65-47dc-a5ce-de7d9c768ee9" />

---

# 🤖 Machine Learning

## 🧠 Model Used
- Logistic Regression

## ⚡ Techniques Applied
- Train-Test Split
- Feature Encoding
- Class Imbalance Handling
- Balanced Class Weights

---

# 📉 Model Evaluation

Evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### 🚨 Important Note
Priority was given to:
- Recall

because missing machine failures can be operationally costly.

---

# 🧰 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SQL
- Power BI

---

# 📂 Repository Structure

```bash
predictive-maintenance-analytics/
│
├── data/
├── notebook/
├── dashboard/
├── screenshots/
├── sql/
└── README.md
```

---

# 🔗 Kaggle Notebook
[KAGGLE NOTEBOOK LINK 🔗.](https://www.kaggle.com/code/mfaiz51826/predictive-maintenance-analysis-failure-predict)

---

# 👨‍💻 Author
Mohammad Faiz Ullah

⭐ If you found this project useful, feel free to star the repository!
