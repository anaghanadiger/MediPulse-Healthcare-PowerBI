# MediPulse-Healthcare-PowerBI

MediPulse is an interactive Power BI dashboard built using the CMS Hospital Compare dataset and a synthetic patient admissions dataset. The dashboard enables healthcare stakeholders to monitor hospital quality, clinical outcomes, and patient experience through interactive visualizations and KPIs.

Dashboard Screenshots
<img width="761" height="429" alt="image" src="https://github.com/user-attachments/assets/c3fa08bd-22b9-472f-8f61-fd3bf3770be3" />
 Hospital Quality Overview

 <img width="762" height="428" alt="image" src="https://github.com/user-attachments/assets/1a0c4bc1-efb3-4292-8e02-9f42a8d59936" />
Readmissions & Clinical Outcomes

<img width="763" height="427" alt="image" src="https://github.com/user-attachments/assets/699bc6e3-4830-4995-a362-64cb8d9cb487" />
Patient Experience

## Key Features

- Star schema data model with dimension and fact tables
- Used Python (Pandas & NumPy) for data cleaning, preprocessing, feature engineering, and generating a synthetic patient admissions dataset.
- Power Query transformations and data cleaning
- Custom Date dimension
- 20+ DAX measures including YTD, YoY Growth, Readmission Rate, Mortality Rate, Good Outcome Rate, and Satisfaction Score
- Interactive slicers and cross-filtering
- Geographic analysis using map visuals
- Conditional formatting for clinical outcome analysis

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

- Synthetic patient admissions dataset (50,000 records) generated in Python for analytical purposes because patient-level admission data is not publicly available.

## How to Use
1. Download `MediPulse_Dashboard.pbix`
2. Open in Power BI Desktop (free at powerbi.microsoft.com)
3. Run `data_preparation.py` to regenerate processed CSVs if needed
4. Re-point data source paths in Power Query → Refresh

## Key Insights

1. **Non-profit hospitals account for over half (54.11%) of all hospitals** in the dataset, making them the dominant ownership type, while for-profit hospitals represent 19.64%.

2. **Renal conditions have the highest 30-day readmission rate (20.73%)**, followed by respiratory (13.22%) and cardiovascular (13.20%) diagnoses, highlighting opportunities to strengthen post-discharge care for these patient groups.

3. **Patient satisfaction scores show minimal variation across insurance types**(range: 7.18–7.20 out of 10), suggesting that perceived care quality is largely independent of a patient's insurance coverage — a positive signal for healthcare equity.
