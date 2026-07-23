# 🏥 Healthcare Operations Analytics Dashboard

An end-to-end healthcare data analytics project focused on analyzing patient demographics, hospital operations, medical conditions, admission patterns, billing performance, and healthcare service utilization.

The project transforms raw healthcare data into actionable business insights using **Python, SQL, and Power BI**.

---

## 📌 Project Overview

Healthcare organizations generate large volumes of operational and patient data. However, raw data often contains missing values, duplicate records, inconsistent text formats, invalid IDs, and data quality issues.

This project focuses on cleaning, validating, analyzing, and visualizing healthcare data to answer important operational and financial questions.

The analysis provides insights into:

* Patient demographics
* Medical conditions
* Admission types
* Hospital performance
* Doctor and patient operations
* Billing amount analysis
* Healthcare cost patterns
* Patient and hospital trends

---

## 🎯 Business Objective

The primary objective of this project is to analyze healthcare operations and identify patterns that can support:

* Improved hospital operational efficiency
* Better understanding of patient admission patterns
* Analysis of billing and healthcare costs
* Identification of high-volume medical conditions
* Improved data-driven decision-making
* Performance monitoring through interactive dashboards

---

## 🛠️ Tools & Technologies

| Tool             | Purpose                                   |
| ---------------- | ----------------------------------------- |
| **Python**       | Data cleaning, transformation, EDA        |
| **Pandas**       | Data manipulation and analysis            |
| **NumPy**        | Numerical operations                      |
| **Matplotlib**   | Data visualization                        |
| **Seaborn**      | Statistical visualization                 |
| **SQL**          | Data querying and KPI analysis            |
| **Power BI**     | Interactive dashboard development         |
| **Excel/CSV**    | Data storage and initial inspection       |
| **Git & GitHub** | Version control and project documentation |

---

## 🔄 Project Workflow

```text
Raw Healthcare Data
        ↓
Data Collection & Inspection
        ↓
Data Cleaning & Standardization
        ↓
Data Validation
        ↓
Feature Engineering
        ↓
Exploratory Data Analysis
        ↓
SQL Analysis & KPI Development
        ↓
Power BI Data Modeling
        ↓
Interactive Dashboard
        ↓
Business Insights & Recommendations
```

---

# 🧹 Data Cleaning & Preparation

The raw healthcare data was cleaned and prepared for analysis using Python.

## 1. Data Inspection

Initial inspection was performed to understand:

* Dataset structure
* Number of rows and columns
* Data types
* Missing values
* Duplicate records
* Unique values
* Potential data quality issues

---

## 2. Missing Value Analysis

Missing values were identified and handled based on the business context and column requirements.

Examples of missing value checks:

```python
df.isnull().sum()
```

Missing values were handled using appropriate techniques such as:

* Imputation
* Replacement with meaningful values
* Removing irrelevant records where appropriate

---

## 3. Text Standardization

Text columns such as patient names, doctors, and hospitals were standardized.

```python
df['Name'] = df['Name'].str.strip().str.title()
df['Doctor'] = df['Doctor'].str.strip().str.title()
df['Hospital'] = df['Hospital'].str.strip().str.title()
```

This helped ensure consistent grouping and accurate analysis.

---

## 4. Duplicate Record Analysis

Duplicate records were identified to improve data accuracy.

```python
df.duplicated().sum()
```

Duplicate records were reviewed and handled appropriately.

---

## 5. ID Validation

Patient, hospital, and doctor IDs were validated to identify unmatched records.

This helped ensure that relationships between healthcare entities were accurate and reliable.

Examples:

* Patient ID validation
* Hospital ID validation
* Doctor ID validation

---

## 6. Derived Columns

New analytical columns were created from existing data to support KPI analysis.

Examples include:

* Length of Stay
* Age Group
* Admission Month
* Billing Category
* Patient Category
* Treatment Duration

---

# 📊 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand patterns and relationships within the healthcare dataset.

## Key Analysis Areas

### 👥 Patient Analysis

* Patient demographics
* Age distribution
* Gender distribution
* Medical condition distribution
* Patient volume trends

### 🏥 Admission Analysis

* Admission type distribution
* Emergency vs planned admissions
* Admission trends
* Medical conditions by admission type

### 💰 Billing Analysis

* Average billing amount
* Billing amount by admission type
* Billing amount by medical condition
* Billing distribution
* Billing amount relationships

### 👨‍⚕️ Healthcare Operations

* Doctor workload
* Hospital patient volume
* Department-level performance
* Operational trends

---

# 📈 Key Visualizations

The project includes multiple visualizations such as:

* Bar Charts
* Count Plots
* Histograms
* KDE Plots
* Box Plots
* Heatmaps
* Time-Series Charts
* Correlation Analysis

Example analysis:

```python
pivot_table = df.pivot_table(
    index='Admission Type',
    columns='Medical Condition',
    values='Billing Amount',
    aggfunc='mean'
)
```

A heatmap was then used to analyze average billing patterns across admission types and medical conditions.

---

# 📌 Key Performance Indicators

The following KPIs were analyzed:

### Patient KPIs

* Total Patients
* Patient Distribution
* Average Patient Age
* Patients by Medical Condition

### Admission KPIs

* Total Admissions
* Admission Type Distribution
* Emergency Admission Rate
* Admission Trends

### Financial KPIs

* Total Billing Amount
* Average Billing Amount
* Billing by Medical Condition
* Billing by Admission Type

### Operational KPIs

* Hospital Patient Volume
* Doctor Patient Load
* Length of Stay
* Medical Condition Distribution

---

# 📊 Power BI Dashboard

The Power BI dashboard provides an interactive view of healthcare operations and performance.

## Dashboard Components

### Executive Overview

Includes:

* Total Patients
* Total Billing Amount
* Average Billing Amount
* Total Hospitals
* Total Doctors
* Medical Conditions

### Patient Analysis

Includes:

* Patient demographics
* Age distribution
* Medical conditions
* Patient volume analysis

### Admission Analysis

Includes:

* Admission type analysis
* Admission trends
* Medical condition by admission type

### Billing Analysis

Includes:

* Average billing by admission type
* Billing by medical condition
* Billing distribution
* Financial performance trends

---

# 🔍 Key Business Questions

This project answers questions such as:

1. Which admission type has the highest average billing amount?
2. Which medical conditions are most common?
3. Which medical conditions generate the highest billing?
4. What is the distribution of patients across hospitals?
5. Which admission types have the highest patient volume?
6. Are there significant differences in billing amounts across medical conditions?
7. What patterns can be observed in healthcare operations?
8. Which areas may require further operational investigation?

---

# 💡 Business Insights

The analysis helps healthcare organizations understand:

* Patient demand patterns
* High-volume medical conditions
* Admission trends
* Billing variations
* Hospital performance
* Operational workload
* Potential areas for efficiency improvement

These insights can support data-driven decisions related to:

* Resource allocation
* Capacity planning
* Operational performance
* Patient service management
* Financial analysis

---

# 📁 Project Structure

```text
Healthcare-Operations-Analytics/
│
├── data/
│   ├── raw/
│   └── cleaned/
│
├── notebooks/
│   ├── 01_Data_Inspection.ipynb
│   ├── 02_Data_Cleaning.ipynb
│   └── 03_Exploratory_Data_Analysis.ipynb
│
├── sql/
│   ├── database_schema.sql
│   └── healthcare_kpis.sql
│
├── powerbi/
│   └── Healthcare_Operations_Analytics.pbix
│
├── visuals/
│   ├── billing_analysis.png
│   ├── admission_analysis.png
│   └── healthcare_dashboard.png
│
├── requirements.txt
└── README.md
```

---

# 🚀 How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/healthcare-operations-analytics.git
```

## 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Or install dependencies using:

```bash
pip install -r requirements.txt
```

## 3. Open the Jupyter Notebook

```bash
jupyter notebook
```

## 4. Run the Analysis

Execute the notebooks in the following order:

1. Data Inspection
2. Data Cleaning
3. Data Validation
4. Feature Engineering
5. Exploratory Data Analysis

## 5. Open the Power BI Dashboard

Open the `.pbix` file using Microsoft Power BI Desktop.

---

# 📚 Skills Demonstrated

This project demonstrates practical experience in:

* Data Cleaning
* Data Preprocessing
* Data Validation
* Exploratory Data Analysis
* Feature Engineering
* Statistical Analysis
* KPI Development
* SQL Querying
* Data Visualization
* Power BI Dashboard Development
* Business Intelligence
* Healthcare Operations Analytics
* Data Storytelling

---

# 🎯 Future Improvements

Future enhancements could include:

* Predicting patient admission volume
* Building a patient readmission prediction model
* Developing healthcare cost prediction models
* Adding time-series forecasting
* Creating automated data pipelines
* Implementing advanced SQL analytics
* Adding machine learning models
* Creating real-time healthcare monitoring dashboards

---

## 👤 Author

**Lingam Nikhil**


⭐ If you find this project useful, feel free to explore the repository and connect with me.
