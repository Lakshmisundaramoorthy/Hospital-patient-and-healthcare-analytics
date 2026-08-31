# Hospital-patient-and-healthcare-analytics
End-to-end healthcare analytics project analyzing 13K+ hospital admission records using Python, SQL, Machine Learning and Power BI. Includes data cleaning, exploratory analysis, hospital KPI analysis, financial and department insights, 30-day readmission risk prediction using Logistic Regression, and an interactive Power BI dashboard.
🏥 Hospital Patient & Healthcare Analytics

An end-to-end healthcare analytics project analyzing 13,266 hospital admission records across two years (January 2024 – December 2025). The project covers data generation, data quality checks, exploratory data analysis, SQL-based business analysis, a 30-day readmission risk prediction model, and an interactive Power BI dashboard.

The objective is to transform hospital admission data into actionable insights around patient demographics, department performance, financial trends, insurance patterns, admission characteristics, and readmission risk.

📌 Project Overview
Goal

Analyze hospital admission data to understand:

Patient demographics and admission patterns
Department performance
Hospital revenue and billing trends
Insurance and admission-type patterns
Length of stay
Patient satisfaction
30-day readmission patterns
Factors associated with readmission risk

In addition, a Logistic Regression model was developed to predict the probability of a patient being readmitted within 30 days.

📊 Dataset

The dataset contains 13,266 hospital admission records covering:

January 2024 – December 2025

The dataset contains 14 fields, including:

Department
Diagnosis
Age
Gender
Insurance Type
Admission Type
Length of Stay
Billing Amount
Discharge Status
30-Day Readmission Flag
Patient Satisfaction

The dataset is synthetically generated for portfolio and learning purposes, with realistic variations in hospital admissions, seasonality, financial patterns, and readmission outcomes.

Note: No real patient data is used in this project.

🎯 Project Objectives
Perform data loading and data quality checks
Identify and handle missing values and duplicate records
Explore patient demographics and admission patterns
Calculate important hospital KPIs
Analyze department-level performance
Analyze financial and billing patterns
Analyze insurance and admission types
Examine patient satisfaction and length-of-stay patterns
Analyze 30-day readmission patterns
Build a machine learning model to predict readmission risk
Create an interactive Power BI dashboard
Generate business-oriented healthcare insights and recommendations
🛠️ Tools & Technologies
Programming & Analysis
Python
Pandas
NumPy
Matplotlib
Seaborn
Database & SQL
SQLite
SQL
Machine Learning
Scikit-learn
Logistic Regression
One-Hot Encoding
StandardScaler
Train-Test Split
ROC-AUC
Classification Report
Visualization & Dashboard
Power BI
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
🔍 1. Data Loading & Data Quality Checks

The project begins by loading the hospital admission dataset using Python and examining its structure.

Data quality checks included:
Dataset shape and structure
Column names and data types
Missing-value analysis
Duplicate record checks
Basic statistical analysis
Categorical-value inspection
Numerical-value distribution checks

The data was then prepared for exploratory analysis and machine learning.

📈 2. Exploratory Data Analysis

Python was used to explore patterns and relationships across the hospital data.

Areas analyzed:
Patient age distribution
Gender distribution
Department-wise admissions
Insurance type distribution
Admission types
Diagnosis patterns
Length of stay
Billing amount
Patient satisfaction
Discharge status
30-day readmission patterns
Monthly and seasonal admission trends
🏥 3. Hospital KPI Analysis

Key hospital performance indicators were calculated to provide an overall view of hospital operations.

KPI	Value
Total Admissions	13,266
Unique Patients	8,436
Total Revenue	₹113.1 Cr
Average Length of Stay	4.57 days
30-Day Readmission Rate	10.60%
Average Patient Satisfaction	3.76 / 5

These KPIs provide a high-level view of hospital activity, financial performance, patient outcomes, and operational trends.

🗄️ 4. SQL Analysis

SQL was used to answer business-oriented questions from the hospital dataset.

SQL analysis includes:
Overall admission and revenue KPIs
Monthly admission trends
Monthly revenue trends
Department performance
Department-wise readmission rates
Age-band analysis
Insurance-type analysis
Discharge status analysis
High-cost admission analysis
Revenue growth analysis
Ranking departments based on performance

SQL techniques used include:

SELECT
WHERE
GROUP BY
ORDER BY
Aggregate functions
CASE WHEN
Common Table Expressions (CTEs)
Window functions
RANK() OVER()
SUM() OVER()

SQL queries are available in:

sql/analysis_queries.sql
🤖 5. Machine Learning — 30-Day Readmission Risk Prediction

A Logistic Regression classification model was developed to predict whether a patient would be readmitted within 30 days.

Target Variable
is_readmission_30d

The target represents whether the patient experienced a readmission within 30 days.

Features Used

The model uses:

Age
Length of Stay
Billing Amount
Department
Insurance Type
Admission Type
Gender
Data Preprocessing

Categorical variables were converted into numerical features using One-Hot Encoding.

Numerical features were standardized using StandardScaler.

The dataset was divided into:

75% Training Data
25% Testing Data

Stratified sampling was used to maintain the class distribution between training and testing datasets.

Because readmissions represent a smaller proportion of the dataset, class_weight='balanced' was used to help address class imbalance.

Model

Logistic Regression — Scikit-learn

The model was selected because its coefficients are relatively interpretable and can help understand how different features are associated with predicted readmission risk.

📊 Model Performance

The model was evaluated on the held-out test dataset.

ROC-AUC

0.81

Additional evaluation metrics include:

Classification Report
Precision
Recall
F1-score
ROC Curve
ROC Curve




The ROC-AUC score of 0.81 indicates good discrimination between patients with and without a 30-day readmission in the test dataset.

This model is intended as an analytical risk-screening exercise for the project and should not be interpreted as a clinical decision-making system.

📊 6. Power BI Dashboard

An interactive Power BI dashboard was developed to provide a visual overview of hospital performance.

The dashboard contains four main pages:

🏥 Executive Overview

Provides a high-level view of hospital KPIs, admissions, revenue, readmission rate and overall performance.




👤 Patient Analysis

Provides insights into patient demographics, admission patterns, age groups, gender and readmission trends.




💰 Financial Analysis

Analyzes hospital revenue, billing amounts, insurance patterns and financial trends.




🏢 Department Performance

Compares departments based on admissions, revenue, length of stay and readmission-related metrics.




💡 7. Key Insights

The analysis identified several important patterns:

1. Seasonal Admission Trends

Hospital admissions and revenue show noticeable seasonal patterns, with higher activity during winter and monsoon periods.

2. Department Performance

Oncology and Orthopedics generate higher revenue per admission, while General Medicine and Emergency contribute significant patient volumes.

3. Readmission Patterns

Readmission rates vary across departments. Pulmonology and General Medicine show relatively higher readmission rates in the analyzed dataset.

These differences can be investigated further to understand potential operational or discharge-related factors.

4. Readmission Risk

The Logistic Regression model achieved a ROC-AUC of 0.81 using routinely available patient and admission characteristics.

5. Patient Satisfaction

Patient satisfaction tends to be lower among patients with longer hospital stays, particularly for stays exceeding approximately 10 days.

These findings are based on the synthetic dataset created for this project and should not be interpreted as conclusions about real-world hospitals.

📌 8. Business Recommendations

Based on the analysis:

Monitor departments with higher patient volumes to support resource planning.
Investigate departments with higher readmission rates to identify potential areas for further analysis.
Monitor high-cost admissions to understand hospital billing and cost drivers.
Track length-of-stay patterns to identify potential operational improvement opportunities.
Monitor patient satisfaction across different length-of-stay groups.
Use readmission-risk predictions as an analytical screening mechanism for identifying patients who may require further review.
📁 9. Project Structure
hospital-patient-healthcare-analytics/
│
├── data/
│   ├── hospital_admissions_data.csv
│   └── generate_data.py
│
├── sql/
│   ├── hospital_analytics.db
│   └── analysis_queries.sql
│
├── notebooks/
│   ├── hospital_analytics.ipynb
│   └── run_analysis.py
│
├── python/
│   ├── 01_data_loading_quality_checks.py
│   ├── 02_eda_analysis.py
│   └── 03_readmission_prediction.py
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
└── README.md
⚙️ 10. How to Run the Project
Python Analysis

Install the required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

Run the notebook:

jupyter notebook notebooks/hospital_analytics.ipynb
SQL Analysis

The SQL database and queries are available in:

sql/

The main SQL query file is:

sql/analysis_queries.sql

The project uses SQLite for database analysis.

Power BI Dashboard

Open:

powerbi/Hospital_Healthcare_Analytics.pbix

using Microsoft Power BI Desktop.

📦 11. Requirements

The main Python dependencies are:

pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter

Install them using:

pip install -r requirements.txt
🚀 12. Future Improvements

Potential future improvements include:

Test the approach on a public healthcare dataset
Compare Logistic Regression with tree-based models such as Random Forest or XGBoost
Perform hyperparameter tuning
Add model explainability techniques
Develop a length-of-stay prediction model
Add additional hospital operational KPIs
Deploy the dashboard as a web application
Monitor model performance over time
💼 13. Resume Project Description

Hospital Patient & Healthcare Analytics | Python, SQL, Machine Learning, Power BI

Built an end-to-end healthcare analytics project using SQL and Python on 13K+ hospital admission records; developed a Logistic Regression model for 30-day readmission risk with a ROC-AUC of 0.81, and built an interactive Power BI dashboard highlighting department performance, financial trends and seasonal admission patterns.

⭐ Skills Demonstrated

Data Analytics:
Data Cleaning · Exploratory Data Analysis · KPI Development · Business Analysis

Programming:
Python · Pandas · NumPy · Matplotlib · Seaborn

Database:
SQL · SQLite · Aggregations · CTEs · Window Functions

Machine Learning:
Logistic Regression · Feature Encoding · Feature Scaling · Classification · ROC-AUC

Visualization:
Power BI · Data Visualization · Interactive Dashboards

📌 Disclaimer

This project uses a synthetically generated healthcare dataset for educational and portfolio purposes. The analysis and machine learning model are not intended for clinical diagnosis, treatment decisions, or real-world patient care.
