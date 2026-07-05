# MediPulse | Healthcare Analytics Dashboard (Power BI)

MediPulse is an end-to-end healthcare analytics project that combines real CMS Hospital Compare data with a Python-generated synthetic patient admissions dataset. The project demonstrates data cleaning, ETL, dimensional modelling, DAX, and interactive dashboard development in Power BI to support hospital quality and operational decision-making.

## Business Questions

This dashboard was built to answer three key questions:

• Which states and hospital types require the greatest quality improvement?

• Which diagnosis categories contribute most to readmissions and mortality?

• Which patient groups are at greater risk, and how does patient experience vary across demographics and insurance providers?

Each dashboard page is designed around one stakeholder question and combines interactive KPIs, visual analytics, and filtering to support operational decision-making.


### Page 1 — Hospital Quality Overview




<img width="765" height="434" alt="PAGE 1" src="https://github.com/user-attachments/assets/342d5b60-b427-4e12-83d0-9ebe82d7f62b" />





### Page 2 — Readmissions & Clinical Outcomes




 
<img width="761" height="434" alt="PAGE 2" src="https://github.com/user-attachments/assets/a70ccdd5-81e3-483b-ba68-b725dd8b502c" />






### Page 3 — Patient Experience & Outcomes






<img width="765" height="432" alt="PAGE 3" src="https://github.com/user-attachments/assets/66b1e5f7-8ff1-4a76-b21e-c21a115520fe" />







## Key Insights

- **Non-profit hospitals account for 54.11% of hospitals** in the dataset, making them the largest ownership group, followed by government (21.45%) and for-profit hospitals (19.64%).

- **Renal conditions have the highest 30-day readmission rate (20.73%)**, considerably higher than other diagnosis categories, highlighting an opportunity to strengthen discharge planning and follow-up care.

- **Hospital quality ratings vary across states**, with average ratings in the displayed comparison ranging from **2.8★ to 3.8★**, demonstrating regional differences in hospital performance.

- **Patients aged 75+ have the highest 30-day readmission rate (13.52%)**, while younger age groups remain below 10%, highlighting older adults as a priority group for post-discharge follow-up.

- **Patient satisfaction remains consistent across insurance types (7.18–7.20/10)**, suggesting a broadly similar patient experience across insurance providers within this dataset.

## Technical Features

| Feature | Implementation |
|---|---|
| Data Modeling | Designed a star schema with 5 tables and 4 relationships |
| Python Data Preparation | Used Python (Pandas & NumPy) for data cleaning, preprocessing, feature engineering, and synthetic patient admissions data generation |
| ETL | Performed data transformation using Power Query (M), including data type conversion, derived columns, and a custom Date dimension |
| DAX Measures | Developed 20+ DAX measures including YTD, YoY Growth, Readmission Rate, Mortality Rate, Good Outcome Rate, Average Length of Stay, and Patient Satisfaction |
| Interactive Dashboard | Built interactive dashboards with slicers, cross-filtering, KPI cards, maps, matrices, and conditional formatting |
| Time Intelligence | Implemented DAX time intelligence using DATESYTD and SAMEPERIODLASTYEAR |
| Dashboard Design | Structured each page around a business question, supported by key findings and stakeholder-focused visualizations |
| Data Source | Combined real CMS Hospital Compare data with a Python-generated synthetic patient admissions dataset for patient-level analysis |

## Tools & Technologies

- **Power BI Desktop**
- **Power Query (M)**
- **DAX**
- **Python (Pandas, NumPy)**
- **Microsoft Excel**

## Data Model

The dashboard follows a star schema consisting of:

- DimHospital
- DimDiagnosis
- DimDate
- FactHospitalQuality
- FactAdmissions

Relationships:
- FactAdmissions → DimHospital
- FactAdmissions → DimDiagnosis
- FactAdmissions → DimDate
- FactHospitalQuality → DimHospital

## Data Source

This project combines:

- CMS Hospital Compare (real public data)
  - Hospital General Information
  - Complications & Deaths
  - HCAHPS
  - Timely & Effective Care

- Python-generated synthetic patient admissions dataset (50,000 records) created to simulate patient-level operational data because CMS Hospital Compare does not publish patient-level admissions.

## Author

Anagha Nadiger

Health Data Analyst | Biotechnology Graduate | Aspiring Data Analyst

www.linkedin.com/in/anagha-nadiger

anaghanadiger@gmail.com
