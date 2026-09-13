# HIMS Analysis

## Hospital Information Management System – Data Analytics Project

### Project Overview

The Hospital Information Management System (HIMS) Analysis is a data analytics project focused on understanding hospital operations through data.

The dataset contains information related to patients, admissions, departments, diseases, diagnostic tests, prescriptions, drugs, inventory, billing, insurance, doctors, and employees.

The main goal of this project is to transform raw hospital data into meaningful insights that can help understand patient patterns, hospital resources, financial performance, inventory status, and clinical information.

The project follows a complete data analytics workflow using:

**Excel → Python → EDA → SQL → Tableau → Insights → Recommendations**

---

## Project Objectives

The main objectives of this project are:

- Understand the structure of the HIMS dataset.
- Clean and prepare the raw data.
- Perform Exploratory Data Analysis (EDA).
- Analyze patient and admission patterns.
- Study patient length of stay.
- Analyze departments and wards.
- Understand diseases and diagnostic results.
- Analyze prescriptions and drugs.
- Study drug inventory and low-stock medicines.
- Analyze hospital billing and financial information.
- Analyze insurance information.
- Study doctors, employees, and staff.
- Create interactive Tableau dashboards.
- Generate useful business insights and recommendations.

---

# Dataset Overview

The HIMS dataset consists of **19 related tables** covering different areas of hospital operations.

Some of the important tables include:

- Patient
- Admission
- Billing
- Billing Details
- Department
- Ward
- Disease
- Diagnostic
- Patient Diagnostic
- Prescription
- Drug
- Inventory
- Patient Insurance
- Doctor
- Employee
- Staff

The major tables contain:

- **30,000 patients**
- **45,000 admissions**
- **45,000 billing records**
- **112,402 billing detail records**
- **63,269 patient diagnostic records**
- **73,109 prescription records**
- **21,613 patient insurance records**
- **250 drugs**
- **500 employees**
- **98 doctors**

---

# Tools and Technologies

## Excel

Excel was used to understand and inspect the raw HIMS dataset.

It helped in:

- Understanding the different tables.
- Checking columns and data types.
- Reviewing the raw records.
- Understanding relationships between tables.

---

## Python

Python was used mainly for **data cleaning and Exploratory Data Analysis (EDA)**.

### Python Libraries Used

- Pandas
- NumPy
- Matplotlib
- Seaborn

Python helped identify missing values, incorrect formats, unusual values, and important patterns in the data.

---

# Exploratory Data Analysis (EDA)

EDA was performed to understand the dataset before conducting deeper SQL analysis.

The main steps were:

### 1. Data Understanding

The tables, columns, number of records, and important variables were studied.

This helped understand what information was available and how different hospital areas were represented in the dataset.

### 2. Data Quality Checking

The data was checked for:

- Missing values
- Duplicate values
- Incorrect formats
- Invalid values
- Unwanted records

Some data-quality problems were identified.

For example:

- An extra **Total row** was present in the admission table.
- Some values in `billing_details.reference_id` were missing.
- Some patient contact numbers had incorrect formats.
- Some contact numbers contained negative values.
- Some bed numbers were incorrectly displayed as dates.
- Duplicate insurance policy numbers were present.

These issues were cleaned or handled before further analysis.

---

# EDA Findings

### Patient Distribution

The dataset contains **30,000 unique patients**.

Gender distribution:

- Male – 15,918
- Female – 13,478
- Other – 604

The analysis shows that the number of male patients is slightly higher than female patients.

---

### Admission Analysis

There are **45,000 admissions** in the dataset.

Admission types were:

- Elective – 26,923 (approximately 60%)
- Emergency – 18,077 (approximately 40%)

This shows that elective admissions are higher than emergency admissions.

---

### Length of Stay

Length of stay was analyzed across different departments.

The overall average length of stay is around **5 days**.

One important finding was that ICU has a much higher average stay, around **10 days**, while some other departments have an average stay of around **4.6–4.7 days**.

This finding was later used for resource-planning recommendations.

---

### Billing Analysis

Billing information was explored by different charge types.

The analysis showed that different charge types contribute differently to the hospital's total billing.

Room charges were found to be the largest contributor to total billing.

---

# SQL Analysis

After completing EDA, SQL was used for deeper analysis.

The HIMS data was loaded into an SQLite database and analyzed using SQL queries.

The SQL analysis was divided into different areas.

---

## 1. Patient Analysis

Patient information was analyzed based on:

- Gender
- Patient counts
- Patient-related information

The analysis confirmed **30,000 unique patients**.

---

## 2. Admission and Length-of-Stay Analysis

Admissions were analyzed based on:

- Admission type
- Department
- Length of stay
- Admission trends

The analysis found:

- 45,000 admissions.
- Approximately 60% elective admissions.
- Approximately 40% emergency admissions.
- Overall average length of stay of around 5.16 days.
- ICU average stay of around 10 days.

---

## 3. Department and Ward Analysis

Departments and wards were analyzed to understand:

- Patient distribution
- Length of stay
- Department-level patterns
- Hospital resource requirements

The ICU stood out because of its significantly higher average length of stay.

---

## 4. Disease Analysis

Disease-related information was analyzed to understand the distribution of diseases among patients.

This helps identify common disease patterns and supports further clinical analysis.

---

## 5. Diagnostic Test Analysis

Diagnostic records were analyzed based on test results.

The dataset contained:

- 31,823 abnormal results
- 31,446 normal results

The analysis also helped identify tests with comparatively high abnormal-result rates.

These tests can be reviewed further by the clinical team.

---

## 6. Prescription and Drug Analysis

Prescription data was analyzed to understand drug usage and prescription patterns.

This was combined with inventory information to understand medicine availability.

---

## 7. Inventory Analysis

There are **250 drugs** in the inventory.

The analysis found:

- 206 drugs – Normal stock
- 44 drugs – Low stock

Therefore:

**44 out of 250 drugs = 17.6% low stock**

This indicates that some medicines require attention from the pharmacy team.

---

## 8. Billing and Financial Analysis

Billing was analyzed to understand the hospital's financial performance.

The total billing amount was approximately:

**₹1.68 billion**

Room charges were the largest contributor to total billing.

The analysis also found a significant amount of pending billing.

Approximately **₹356.4 million** was pending.

This indicates an opportunity for better billing follow-up and collection.

---

## 9. Insurance Analysis

Patient insurance information was analyzed to understand insurance-related records and payment patterns.

Insurance was also identified as the major payment method in the billing data.

---

## 10. Staff and Doctor Analysis

The employee and doctor information was analyzed to understand hospital staffing.

The dataset contains:

- 500 employees
- 98 doctors

Employee roles included:

- Nurses
- Pharmacists
- Doctors
- Technicians
- Administrators

This analysis can support understanding of hospital workforce distribution.

---

# Tableau Dashboard

After completing Python EDA and SQL analysis, the major findings were presented using Tableau.

The dashboards were designed to make the information easier to understand through charts, KPIs, and visualizations.

## Dashboards Created

### 1. Hospital Executive Overview

This dashboard provides a high-level view of hospital performance.

It helps understand:

- Patient and admission numbers
- Billing information
- Hospital activity
- Key performance indicators

---

### 2. Patient & Admission Analysis

This dashboard focuses on:

- Patient distribution
- Admission types
- Admission trends
- Length of stay
- Department-level information

It helps users understand patient and admission patterns.

---

### 3. Disease & Clinical Analysis

This dashboard focuses on clinical information such as:

- Disease patterns
- Diagnostic tests
- Normal and abnormal results
- Clinical trends

It helps provide a better understanding of the clinical side of the hospital.

---

# Key Business Insights

The major insights from the complete analysis are:

### Insight 1 – ICU stays are longer

ICU patients have an average stay of around **10 days**, which is much higher than some other departments.

This makes ICU resource planning important.

---

### Insight 2 – Many bills are pending

A significant amount of billing is still pending, with approximately **₹356.4 million** identified as pending.

Better follow-up can improve financial collection.

---

### Insight 3 – Room charges generate major revenue

Room charges contribute the largest share of the hospital's total billing.

This makes room occupancy and room-related revenue important areas to monitor.

---

### Insight 4 – Some drugs are low in stock

**44 out of 250 drugs (17.6%)** are classified as low stock.

This creates a clear requirement for pharmacy inventory monitoring and timely reordering.

---

### Insight 5 – Diagnostic abnormalities need review

Some diagnostic tests show comparatively high abnormal-result rates.

These results can be investigated further to understand whether there are meaningful clinical patterns.

---

# Recommendations

Based on the analysis, the following recommendations were made.

## 1. Review ICU Throughput

ICU patients have a much longer average stay than some other departments.

The hospital should investigate the reasons for longer ICU stays and use this information for better planning of:

- ICU beds
- Medical staff
- Equipment
- Medicines
- Other ICU resources

---

## 2. Target Bill Collections

A large amount of billing is pending.

The hospital should focus on outstanding bills and improve payment follow-up.

This can help improve financial collection and cash flow.

---

## 3. Plan Drug Reordering

Since **17.6% of drugs are low in stock**, the pharmacy team should prioritize these medicines for reordering.

Regular inventory monitoring can help prevent medicine shortages.

---

## 4. Investigate High-Abnormal-Rate Tests

Diagnostic tests with high abnormal-result rates should be reviewed by the clinical team.

This can help identify important clinical patterns and ensure that unusual results are properly understood.

---

# Project Workflow

The complete project workflow was:

```text
Raw HIMS Excel Dataset
          ↓
Data Understanding
          ↓
Data Cleaning
          ↓
Exploratory Data Analysis
          ↓
SQL Database Creation
          ↓
SQL Analysis
          ↓
Business Insights
          ↓
Tableau Visualization
          ↓
Recommendations




## 🤝 Community Service Project

As part of my academic work, I participated in a community service project. This experience helped me develop teamwork, communication, responsibility, and social awareness.

### 📸 Community Service Activities

[![Community Service Activity 1](https://github.com/nandinipadidham-lgtm/HIMS-Analysis/blob/main/cs1.jpeg)](https://github.com/nandinipadidham-lgtm/HIMS-Analysis/blob/main/cs1.jpeg)

[![Community Service Activity 2](https://github.com/nandinipadidham-lgtm/HIMS-Analysis/blob/main/cs2.jpeg)](https://github.com/nandinipadidham-lgtm/HIMS-Analysis/blob/main/cs2.jpeg)

