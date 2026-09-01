# Hospital-patient-and-healthcare-analytics
End-to-end healthcare analytics project analyzing 13K+ hospital admission records using Python, SQL, Machine Learning and Power BI. Includes data cleaning, exploratory analysis, hospital KPI analysis, financial and department insights, 30-day readmission risk prediction using Logistic Regression, and an interactive Power BI dashboard.
🏥 Hospital Patient & Healthcare Analytics

End-to-end healthcare analytics project using Python, SQL, Machine Learning and Power BI

Analyzed 13,266 hospital admission records across January 2024 – December 2025 to identify hospital performance trends, patient patterns, financial insights, department performance and 30-day readmission risk.

🎯 Project Objective

The project focuses on answering important healthcare business questions:

🏥 How is the hospital performing overall?
👥 What are the major patient demographic patterns?
💰 Which departments and areas generate the most revenue?
📊 How do admissions change over time?
🏢 Which departments have higher admission and readmission rates?
💳 How do insurance types affect hospital activity?
⏱️ How does length of stay relate to patient satisfaction?
🤖 Can 30-day readmission risk be predicted using available patient information?
📊 Dataset
Information	Value
Total Admission Records	13,266
Unique Patients	8,436
Period	Jan 2024 – Dec 2025
Number of Fields	14
30-Day Readmission Rate	10.60%
Average Length of Stay	4.57 days
Average Patient Satisfaction	3.76 / 5
Dataset Fields

Admission ID · Admission Date · Department · Diagnosis · Age · Gender · Insurance Type · Admission Type · Length of Stay · Billing Amount · Discharge Status · 30-Day Readmission · Patient Satisfaction

⚠️ The dataset is synthetically generated for educational and portfolio purposes. No real patient data is used.

🛠️ Technologies Used
Area	Technologies
Programming	Python
Data Analysis	Pandas, NumPy
Visualization	Matplotlib, Seaborn
Database	SQLite
SQL	SQL, CTEs, Window Functions
Machine Learning	Scikit-learn
ML Model	Logistic Regression
Dashboard	Microsoft Power BI
🔄 Project Workflow
📥 Hospital Admission Data
        ↓
🔍 Data Loading
        ↓
✅ Data Quality Checks
        ↓
🧹 Data Cleaning & Preparation
        ↓
📊 Exploratory Data Analysis
        ↓
🏥 Hospital KPI Analysis
        ↓
🗄️ SQL Business Analysis
        ↓
🤖 Machine Learning
        ↓
📈 30-Day Readmission Prediction
        ↓
📊 Power BI Dashboard
        ↓
💡 Insights & Recommendations
📌 Analysis Performed
1️⃣ Data Loading & Quality Checks

Python was used to load and inspect the hospital admission dataset.

Checks performed
Dataset shape and structure
Column names and data types
Missing values
Duplicate records
Categorical values
Numerical distributions
Basic statistical analysis
2️⃣ Exploratory Data Analysis

The dataset was analyzed to understand:

👥 Patient age distribution
⚥ Gender distribution
🏢 Department-wise admissions
💳 Insurance type distribution
🚑 Admission types
🩺 Diagnosis patterns
⏱️ Length of stay
💰 Billing amounts
⭐ Patient satisfaction
🔄 30-day readmissions
📅 Monthly admission trends
🌦️ Seasonal patterns
🏥 Hospital KPI Overview
KPI	Result
Total Admissions	13,266
Unique Patients	8,436
Total Revenue	₹113.1 Cr
Average Length of Stay	4.57 days
30-Day Readmission Rate	10.60%
Average Satisfaction	3.76 / 5
🗄️ SQL Business Analysis

SQL was used to answer business-oriented questions from the hospital dataset.

Analysis includes
📊 Admission and revenue KPIs
📅 Monthly admission trends
💰 Monthly revenue trends
🏢 Department performance
🔄 Department-wise readmission rates
👥 Age-band analysis
💳 Insurance-type analysis
🏥 Discharge-status analysis
💰 High-cost admissions
📈 Revenue growth
🏆 Department ranking
SQL Concepts Used
SELECT
WHERE
GROUP BY
ORDER BY
Aggregate Functions
CASE WHEN
CTEs
Window Functions
RANK() OVER()
SUM() OVER()

📁 SQL file:

sql/analysis_queries.sql
🤖 Machine Learning — 30-Day Readmission Prediction

A Logistic Regression model was developed to predict whether a patient would be readmitted within 30 days.

🎯 Target
is_readmission_30d
📥 Features Used
Age
Length of Stay
Billing Amount
Department
Insurance Type
Admission Type
Gender
🔧 Preprocessing

Categorical variables were converted using One-Hot Encoding.

Numerical variables were standardized using StandardScaler.

The dataset was split into:

Dataset	Percentage
Training	75%
Testing	25%

Stratified sampling was used to maintain the class distribution.

Because readmission is a minority class,:

class_weight='balanced'

was used.

📈 Model Performance
Logistic Regression

ROC-AUC: 0.81

The model was evaluated on the held-out test dataset using:

ROC-AUC
Precision
Recall
F1-score
Classification Report
ROC Curve
ROC Curve




The model is an analytical risk-screening exercise for this portfolio project and is not intended for clinical decision-making.

📊 Power BI Dashboard

An interactive Power BI dashboard was created with 4 analytical pages.

🏥 Executive Overview

Provides an overall view of:

Total admissions
Revenue
Readmission rate
Patient satisfaction
Hospital performance




👤 Patient Analysis

Analyzes:

Patient demographics
Age groups
Gender
Admission patterns
Readmission trends




💰 Financial Analysis

Analyzes:

Hospital revenue
Billing amounts
Insurance patterns
Financial trends
Cost-related insights




🏢 Department Performance

Compares departments based on:

Admissions
Revenue
Length of stay
Readmission metrics




💡 Key Insights
1. 📅 Seasonal Trends

Admissions and revenue show noticeable seasonal patterns, with higher activity during winter and monsoon periods.

2. 🏢 Department Performance

Oncology and Orthopedics generate higher revenue per admission, while General Medicine and Emergency contribute significant patient volumes.

3. 🔄 Readmission Patterns

Readmission rates vary across departments, with Pulmonology and General Medicine showing relatively higher rates in this dataset.

4. 🤖 Readmission Risk

The Logistic Regression model achieved a ROC-AUC of 0.81 using routinely available patient and admission characteristics.

5. ⭐ Patient Satisfaction

Patient satisfaction tends to decrease among patients with longer hospital stays, particularly for stays exceeding approximately 10 days.

These findings are based on the synthetic dataset used in this project and should not be interpreted as conclusions about real-world hospitals.

📌 Business Recommendations

Based on the analysis:

📊 Monitor high-volume departments for resource planning.
🔄 Investigate departments with higher readmission rates.
💰 Monitor high-cost admissions to identify cost drivers.
⏱️ Analyze length-of-stay patterns for operational improvement.
⭐ Track patient satisfaction across length-of-stay groups.
🤖 Use readmission-risk predictions as an analytical screening mechanism for further review.
📁 Project Structure
Hospital-patient-and-healthcare-analytics/
│
├── 📁 data/
│   └── hospital_admissions_data.csv
│
├── 📁 notebooks/
│   └── hospital_analytics.ipynb
│
├── 📁 sql/
│   └── analysis_queries.sql
│
├── 📁 powerbi/
│   └── Hospital_Healthcare_Analytics.pbix
│
├── 📁 screenshots/
│   ├── executive_overview.png
│   ├── patient_analysis.png
│   ├── financial_analysis.png
│   └── department_performance.png
│
├── 📁 outputs/
│   └── readmission_model_roc.png
│
├── 📄 requirements.txt
├── 📄 LICENSE
├── 📄 .gitignore
└── 📄 README.md
⚙️ How to Run
🐍 Python Analysis

Install the required libraries:

pip install -r requirements.txt

Open the notebook:

jupyter notebook notebooks/hospital_analytics.ipynb
🗄️ SQL Analysis

SQL queries are available here:

sql/analysis_queries.sql

The project uses SQLite for database analysis.

📊 Power BI

Download:

powerbi/Hospital_Healthcare_Analytics.pbix

Open the file using Microsoft Power BI Desktop.

GitHub may not preview large .pbix files in the browser. The Power BI screenshots above provide a visual preview of the dashboard.

📦 Requirements

Main Python dependencies:

pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter

Install using:

pip install -r requirements.txt
🚀 Future Improvements
Use a public healthcare dataset for further validation.
Compare Logistic Regression with Random Forest/XGBoost.
Perform hyperparameter tuning.
Add model explainability.
Develop a length-of-stay prediction model.
Add additional hospital operational KPIs.
Deploy the dashboard as a web application.
💼 Resume Description

Hospital Patient & Healthcare Analytics | Python, SQL, Machine Learning, Power BI

Built an end-to-end healthcare analytics project on 13K+ hospital admission records using Python and SQL; developed a Logistic Regression model for 30-day readmission risk with ROC-AUC 0.81, and created an interactive Power BI dashboard highlighting hospital KPIs, department performance, financial trends and seasonal admission patterns.

⭐ Skills Demonstrated

Data Analytics: Data Cleaning · EDA · KPI Development · Business Analysis

Python: Pandas · NumPy · Matplotlib · Seaborn

SQL: SQLite · Aggregations · CTEs · Window Functions · Ranking

Machine Learning: Logistic Regression · One-Hot Encoding · StandardScaler · Classification · ROC-AUC

Visualization: Power BI · Interactive Dashboards

⚠️ Disclaimer

This project uses a synthetically generated healthcare dataset for educational and portfolio purposes.

The analysis and machine learning model are not intended for clinical diagnosis, treatment decisions, or real-world patient care.
