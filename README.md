# Hospital-patient-and-healthcare-analytics
End-to-end healthcare analytics project analyzing 13K+ hospital admission records using Python, SQL, Machine Learning and Power BI. Includes data cleaning, exploratory analysis, hospital KPI analysis, financial and department insights, 30-day readmission risk prediction using Logistic Regression, and an interactive Power BI dashboard.
🏥 Hospital Patient & Healthcare Analytics

An end-to-end healthcare analytics project analyzing 13,266 hospital admission records across 2024–2025 using Python, SQL, Machine Learning, and Power BI.

The project covers data quality checks, exploratory data analysis, hospital KPI analysis, SQL business analysis, financial and department insights, 30-day readmission risk prediction, and an interactive Power BI dashboard.

Note: This project uses a synthetically generated healthcare dataset for educational and portfolio purposes. No real patient data is used.

🎯 Project Objective

The goal is to transform hospital admission data into actionable insights around:

Patient demographics and admission patterns
Department performance
Hospital revenue and billing
Insurance and admission types
Length of stay
Patient satisfaction
30-day readmission patterns
Readmission risk prediction
📊 Dataset
Details	Value
Admission Records	13,266
Period	Jan 2024 – Dec 2025
Unique Patients	8,436
Number of Fields	14

Key fields include:

Admission ID · Admission Date · Department · Diagnosis · Age · Gender · Insurance Type · Admission Type · Length of Stay · Billing Amount · Discharge Status · 30-Day Readmission · Patient Satisfaction

🛠️ Tools & Technologies

Python

Pandas
NumPy
Matplotlib
Seaborn

SQL

SQLite
Aggregations
CASE WHEN
CTEs
Window Functions
RANK()

Machine Learning

Scikit-learn
Logistic Regression
One-Hot Encoding
StandardScaler
Train-Test Split
ROC-AUC
Classification Report

Visualization

Microsoft Power BI
🔄 Project Workflow
Hospital Admission Data
        ↓
Data Loading
        ↓
Data Quality Checks
        ↓
Data Cleaning & Preparation
        ↓
Exploratory Data Analysis
        ↓
Hospital KPI Analysis
        ↓
SQL Business Analysis
        ↓
Machine Learning
        ↓
30-Day Readmission Prediction
        ↓
Power BI Dashboard
        ↓
Insights & Recommendations
🔍 1. Data Quality & Exploratory Analysis

Python was used for:

Dataset structure and data-type checks
Missing-value analysis
Duplicate-record checks
Statistical analysis
Categorical-value inspection
Numerical distribution analysis
Patient demographic analysis
Department analysis
Insurance analysis
Admission-type analysis
Length-of-stay analysis
Billing analysis
Patient satisfaction analysis
Readmission analysis
Monthly and seasonal trend analysis
🏥 2. Hospital KPI Overview
KPI	Value
Total Admissions	13,266
Unique Patients	8,436
Total Revenue	₹113.1 Cr
Average Length of Stay	4.57 days
30-Day Readmission Rate	10.60%
Average Patient Satisfaction	3.76 / 5

These KPIs provide a high-level view of hospital activity, financial performance, patient outcomes, and operational trends.

🗄️ 3. SQL Business Analysis

SQL was used to answer business-oriented healthcare questions including:

Overall admission and revenue KPIs
Monthly admission trends
Monthly revenue trends
Department performance
Department-wise readmission rates
Age-band analysis
Insurance-type analysis
Discharge-status analysis
High-cost admissions
Revenue growth
Department ranking

SQL techniques include:

SELECT · WHERE · GROUP BY · ORDER BY · Aggregate Functions · CASE WHEN · CTEs · Window Functions · RANK() OVER()

SQL queries are available in:

sql/analysis_queries.sql

🤖 4. Machine Learning — 30-Day Readmission Risk

A Logistic Regression classification model was developed to predict whether a patient would experience a readmission within 30 days.

Target Variable

is_readmission_30d

Features
Age
Length of Stay
Billing Amount
Department
Insurance Type
Admission Type
Gender
Data Preparation

Categorical variables were converted into numerical variables using One-Hot Encoding.

Numerical variables were standardized using StandardScaler.

The dataset was split using:

75% Training
25% Testing
Stratified sampling
class_weight='balanced'
Model Performance

ROC-AUC: 0.81

The model demonstrates good discrimination between patients with and without a 30-day readmission in the held-out test dataset.

The model is intended as an analytical risk-screening exercise, not as a clinical decision-making system.

ROC Curve




📊 5. Power BI Dashboard

An interactive Power BI dashboard was created with four main analytical pages.

🏥 Executive Overview

High-level hospital KPIs, admissions, revenue, readmission rate, and overall performance.




👤 Patient Analysis

Patient demographics, age groups, gender, admission patterns, and readmission trends.




💰 Financial Analysis

Revenue, billing amounts, insurance patterns, and financial trends.




🏢 Department Performance

Department-level admissions, revenue, length of stay, and readmission metrics.




💡 6. Key Insights
1. Seasonal Admission Trends

Admissions and revenue show noticeable seasonal patterns, with higher activity during winter and monsoon periods.

2. Department Performance

Oncology and Orthopedics generate higher revenue per admission, while General Medicine and Emergency contribute significant patient volumes.

3. Readmission Patterns

Readmission rates vary across departments, with Pulmonology and General Medicine showing relatively higher rates in this dataset.

4. Readmission Risk

The Logistic Regression model achieved a ROC-AUC of 0.81 using routinely available patient and admission characteristics.

5. Patient Satisfaction

Patient satisfaction tends to decrease among patients with longer hospital stays, particularly for stays exceeding approximately 10 days.

These findings are based on the synthetic dataset and should not be interpreted as conclusions about real-world hospitals.

📌 7. Business Recommendations
Monitor high-volume departments for resource planning.
Investigate departments with higher readmission rates.
Monitor high-cost admissions to identify billing and cost drivers.
Analyze length-of-stay patterns for operational improvement.
Track patient satisfaction across length-of-stay groups.
Use readmission-risk predictions as an analytical screening mechanism for further review.
📁 8. Project Structure
Hospital-patient-and-healthcare-analytics/
│
├── data/
│   └── hospital_admissions_data.csv
│
├── notebooks/
│   └── hospital_analytics.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── powerbi/
│   └── Hospital_Healthcare_Analytics.pbix
│
├── screenshots/
│   ├── executive_overview.png
│   ├── patient_analysis.png
│   ├── financial_analysis.png
│   └── department_performance.png
│
├── outputs/
│   └── readmission_model_roc.png
│
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
⚙️ 9. How to Run
Python

Install the required libraries:

pip install -r requirements.txt

Open the notebook:

jupyter notebook notebooks/hospital_analytics.ipynb
SQL

The SQL queries are available in:

sql/analysis_queries.sql

The project uses SQLite for database analysis.

Power BI

Download the .pbix file from:

powerbi/Hospital_Healthcare_Analytics.pbix

Open it using Microsoft Power BI Desktop.

📦 10. Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter

Install with:

pip install -r requirements.txt
🚀 11. Future Improvements
Test the approach using a public healthcare dataset.
Compare Logistic Regression with Random Forest or XGBoost.
Perform hyperparameter tuning.
Add model explainability techniques.
Develop a length-of-stay prediction model.
Add additional hospital operational KPIs.
Deploy the dashboard as a web application.
💼 Resume Project Description

Hospital Patient & Healthcare Analytics | Python, SQL, Machine Learning, Power BI

Built an end-to-end healthcare analytics project on 13K+ hospital admission records using Python and SQL; developed a Logistic Regression model for 30-day readmission risk with ROC-AUC 0.81, and built an interactive Power BI dashboard highlighting hospital KPIs, department performance, financial trends, and seasonal admission patterns.

⭐ Skills Demonstrated

Data Analytics: Data Cleaning · EDA · KPI Development · Business Analysis

Programming: Python · Pandas · NumPy · Matplotlib · Seaborn

Database: SQL · SQLite · CTEs · Window Functions · Aggregations

Machine Learning: Logistic Regression · One-Hot Encoding · StandardScaler · Classification · ROC-AUC

Visualization: Power BI · Interactive Dashboards

📌 Disclaimer

This project uses a synthetically generated healthcare dataset for educational and portfolio purposes. The analysis and machine learning model are not intended for clinical diagnosis, treatment decisions, or real-world patient care.
