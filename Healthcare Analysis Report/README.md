# Healthcare Analytics Dashboard – Power BI Project

## Project Overview

Developed a comprehensive Healthcare Analytics Dashboard in Power BI to monitor patient activity, doctor performance, treatment effectiveness, operational efficiency, and revenue generation. The project focuses on transforming healthcare data into meaningful business insights through interactive dashboards and advanced analytics.

---

## Business Objective

The main objective of this project is to help healthcare organizations analyze operational performance, improve patient management, monitor doctor efficiency, and track revenue trends using data-driven reporting.

---

## Data Sources

The project uses multiple healthcare-related datasets:

* Patients (1000 records)
* Doctors (1000 records)
* Appointments (1000 records)
* Treatments (1000 records)
* Billing (1000 records)

---

## Data Modeling

Implemented a Star Schema model with the following relationships:

* Patients[PatientID] → Appointments[PatientID]
* Doctors[DoctorID] → Appointments[DoctorID]
* Appointments[AppointmentID] → Treatments[AppointmentID]
* Appointments[AppointmentID] → Billing[AppointmentID]

---

## Power Query Transformations

Performed multiple data cleaning and transformation tasks using Power Query:

* Merge Queries for combining Patients, Doctors, and Appointments data
* Append Queries for historical and current datasets
* Removed duplicates and handled null values
* Changed data types and split columns
* Created conditional columns and Age Group categories

---

## DAX Calculations

Created business KPIs and measures using DAX:

* Total Revenue
* Total Treatments
* Average Treatment Cost
* Cancellation Rate %
* Revenue by Department

---

## Drill Down & Interactivity

Implemented drill-down functionality for deeper analysis:

* Year → Quarter → Month → Day hierarchy
* Department → Doctor → Patient hierarchy

Configured Edit Interactions to control filtering behavior across visuals.

---

## Row Level Security (RLS)

Implemented Row Level Security based on DoctorID to restrict doctors from viewing data outside their assigned patients and revenue records.

---

## Dashboard Pages

The report includes the following interactive dashboard pages:

* Executive Overview
* Doctor Performance
* Patient Demographics
* Operational Efficiency

---

## Key KPIs

* Total Patients
* Total Revenue
* Appointment Completion Rate
* Average Treatment Cost
* Male vs Female Patients
* Appointments cancelled/missed

---

## Tools & Technologies

* Power BI
* Power Query
* DAX
* Data Modeling
* Star Schema
* Row Level Security (RLS)

---

## Project Outcome

The dashboard enables healthcare stakeholders to monitor operational performance, identify trends, improve treatment tracking, optimize doctor performance, and support data-driven business decisions through interactive visual analytics.

