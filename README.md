 Hospital-Data-SQL-Analysis
SQL project analyzing hospital data for insights on departments, expenses, and patient statistics.
 Hospital Data Analysis using SQL

SQL Portfolio Project by Insherah Majid

This project demonstrates SQL data analysis on hospital data to explore key business insights such as patient count, department efficiency, and medical expenses.

---

Objective
To analyze hospital performance and patient data using SQL queries — focusing on aggregation, grouping, filtering, and date-based analytics.

---

 Dataset Overview
Table Name:** `hospital`

| Column | Type | Description |
|---------|------|--------------|
| Hospital_Name | varchar(100) | Name of the hospital |
| Location | varchar(50) | City or region |
| Department | varchar(50) | Hospital department |
| Doctors_Count | integer | Total doctors available |
| Patients_Count | numeric | Number of patients |
| Admission_Date | date | Date of admission |
| Discharge_Date | date | Date of discharge |
| Medical_Expenses | numeric(10,2) | Total medical expenses |

---
Table Creation & Data Import

```sql
CREATE TABLE hospital (
    Hospital_Name varchar(100),
    Location varchar(50),
    Department varchar(50),
    Doctors_Count integer,
    Patients_Count numeric,
    Admission_Date date,
    Discharge_Date date,
    Medical_Expenses numeric(10,2)
);

-- Import data from CSV
COPY hospital(Hospital_Name, Location, Department, Doctors_Count, Patients_Count, Admission_Date, Discharge_Date, Medical_Expenses)
FROM 'C:\Users\Nyla Majid\OneDrive\Documents\sql\Hospital_Data.csv'
CSV HEADER;
