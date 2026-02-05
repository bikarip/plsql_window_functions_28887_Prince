# Zed Hospital SQL Analytics Project
**Course:** Database Development with PL/SQL

**Student name:** BIKARI Prince

**Student ID:** 28887

## TABLE OF CONTENTS

1. [Business Problem](#1-business-problem)
2. [Success Criteria](#2-success-criteria)
3. [Database Schema Design](#3-database-schema-design)
4. [Entity Relationship Diagram](#4-entity-relationship-diagram)
5. [SQL JOINs Implementation](#5-sql-joins-implementation)
6. [SQL Window Functions Implementation](#6-sql-window-functions-implementation)
7. [Results Analysis](#7-results-analysis)
8. [Key Insights](#8-key-insights)
9. [References](#9-references)
10. [Integrity Statement](#10-integrity-statement)

---
## 1. Business Problem
### Business Context
Zed General Hospital handles a high number of patient visits across several specialized departments, including Cardiology, Pediatrics, and General Medicine. 
### Data Challenge
Hospital administrators lack clear information about patient visit trends, doctor workload, and department performance. Patient registration data is not well connected to appointment records, making it hard to identify service gaps, evaluate department efficiency, and detect possible revenue loss from inactive patients.
### Expected Outcome
This project combines patient and appointment data to generate useful insights, including identifying the top three revenue-generating doctors, grouping patients by spending levels for targeted programs, and analyzing monthly visit trends to support staff planning for 2026.
## 2. Success Criteria
The project achieves exactly five measurable goals using specific Window Functions:

1.  **Top Performance:** Identify top-performing hospital departments/doctors based on patient visit revenue using RANK().
2.  **Financial Trajectory:** Calculate running totals of hospital revenue over the fiscal year using SUM() OVER().
3.  **Growth Tracking:** Compare month-over-month patient visit changes to detect trends using LAG().
4.  **Patient Segmentation:** Segment patients into 4 quartiles based on visit frequency and cost using NTILE(4).
5.  **Operational Smoothing:** Analyze 3-day moving averages of patient visits to assist in nurse scheduling using
   AVG() OVER().
## 3. Database Schema Design
The database is designed to support hospital operational analysis and consists of three main tables:

* *Patients* (PatientID, FirstName, LastName, City, DateOfBirth) – Stores individual personal and registration data.
* *Doctors* (DoctorID, FirstName, LastName, Specialty, HireDate) – Stores healthcare provider data.
* *Visits* (VisitID, PatientID, DoctorID, VisitDate, VisitCost) – Records transactional visit data.
  ### ER-DIAGRAM
  

