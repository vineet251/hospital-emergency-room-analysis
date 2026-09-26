# 🏥 Hospital Emergency Room Analysis Dashboard

## 📊 Project Overview

This project focuses on analyzing Hospital Emergency Room data and creating an interactive dashboard in Microsoft Excel.

The dashboard provides a clear overview of patient volume, admission status, waiting time, patient satisfaction, age distribution, gender distribution, and department referrals.

The goal of this project is to transform raw hospital emergency room data into meaningful insights that can help stakeholders understand patient flow and identify important operational patterns.

---

## 🎯 Project Objective

The main objective of this project is to analyze Emergency Room patient data and create an interactive Excel dashboard that helps users understand:

- Total number of patients
- Patient admission status
- Average patient waiting time
- Patient satisfaction score
- Patient age distribution
- Gender distribution
- Patient timeliness
- Department referrals
- Monthly patient trends

---

## 🏥 Business Problem

Hospital emergency departments handle a large number of patients every day.

Without proper analysis, it can be difficult to understand:

- How many patients are being admitted
- How many patients are not admitted
- How long patients are waiting
- Which age groups visit the emergency room most frequently
- Which departments receive the most referrals
- Whether patients are being attended to within the expected time
- How satisfied patients are with the service

This project converts raw patient data into an interactive dashboard so that these patterns can be analyzed more easily.

---

## 🛠️ Tools & Technologies

The project was developed using:

- Microsoft Excel
- Power Query
- Power Pivot
- DAX
- Pivot Tables
- Pivot Charts
- Excel Dashboard Design
- Data Cleaning
- Data Analysis
- Data Visualization

---

## 🔄 Project Workflow

The project followed an end-to-end data analysis workflow:

1. Business Requirement Gathering
2. Understanding the Data
3. Data Import using Power Query
4. Data Cleaning
5. Data Quality Checking
6. Calendar Table Creation
7. Data Modeling using Power Pivot
8. Creating Calculated Columns using DAX
9. Creating Pivot Tables
10. Dashboard Layout Design
11. Chart Development
12. Dashboard Development
13. Insight Generation

---

## 📌 Key KPIs

### 👥 Total Patients

The dashboard displays the total number of patients included in the analysis.

### ⏱️ Average Wait Time

Measures the average amount of time patients waited before being attended to.

### ⭐ Patient Satisfaction Score

Shows the average satisfaction score provided by patients.

### 🏥 Admission Status

Shows the number and percentage of:

- Admitted Patients
- Not Admitted Patients

### 👨‍⚕️ Department Referrals

Shows which departments receive the highest number of patient referrals.

---

## 📈 Dashboard Analysis

The dashboard contains several analytical views.

### 1. Patient Admission Status

Shows the comparison between admitted and non-admitted patients.

### 2. Patient Age Distribution

Patients are grouped into different age groups to understand the distribution of emergency room visits.

### 3. Timeliness Analysis

Analyzes whether patients were attended to within the defined waiting-time threshold.

### 4. Gender Analysis

Shows the distribution of patients by gender.

### 5. Department Referral Analysis

Shows the departments to which patients were referred and identifies departments with higher referral volumes.

### 6. Monthly Analysis

Allows users to analyze patient activity by month.

### 7. Year Filter

The dashboard includes a year selection option to make the analysis interactive.

---
Patient Attend Status =
IF(
    [Patient Waittime] < 30,
    "Within Time",
    "Delay"
)

## 🧮 DAX Calculations

### Age Group

The project uses a calculated field to categorize patients into age groups.

Example:

```DAX
Age Group =
IF([Patient Age] >= 70,
    "70-79",
IF([Patient Age] >= 60,
        "60-69",
IF([Patient Age] >= 45,
        "45-59",
IF([Patient Age] >= 30,
        "30-44",
IF([Patient Age] >= 15,
        "15-29",
IF([Patient Age] >= 5,
         "05-14",
          "0-4"))))))
