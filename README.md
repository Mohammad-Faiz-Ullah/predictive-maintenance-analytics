# Predictive Maintenance Analytics & Failure Prediction

## Project Overview
This project focuses on predictive maintenance analytics using industrial machine sensor data. The workflow combines data analytics, business intelligence, and machine learning to identify machine failure patterns and support proactive maintenance decisions.

---

# Objectives
- Analyze machine operational behavior
- Identify failure patterns and high-risk conditions
- Build business-oriented maintenance insights
- Predict machine failure using machine learning
- Create interactive analytical dashboards

---

# Workflow
- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Failure Pattern Analysis
- Feature Engineering
- SQL Analytics
- Power BI Dashboarding
- Logistic Regression Model Training
- Model Evaluation

---

# Exploratory Data Analysis
Performed:
- Univariate & Multivariate Analysis
- Correlation Analysis
- Outlier Detection
- Class Imbalance Analysis
- Sensor Threshold Analysis
- Failure Pattern Visualization

Key findings:
- High torque and tool wear strongly influence machine failures
- Failure probability increases under operational stress
- Dataset is highly imbalanced

---

# Feature Engineering
Created additional operational features:
- `power`
- `temp_diff`

Applied:
- normalization
- feature transformation

---

# SQL Analytics
SQL was used for:
- Failure rate analysis
- Product-wise failure analysis
- KPI extraction
- High-risk machine identification

### Sample SQL Query

```sql
SELECT Type, COUNT(*) AS failures
FROM predictive_maintenance
WHERE `Machine failure` = 1
GROUP BY Type;
