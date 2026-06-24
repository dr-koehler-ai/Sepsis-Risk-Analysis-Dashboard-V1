# Clinical Sepsis Analytics Dashboard

## Project Overview

This project analyzes a large-scale ICU electronic health record dataset to explore clinical patterns associated with sepsis development.

The goal is to identify physiological differences between septic and non-septic patients using real-world longitudinal ICU data and to build a simple clinical analytics workflow.

Rather than focusing on complex machine learning models, this project emphasizes:

- Data understanding of ICU time-series data  
- Clinical interpretation of laboratory and vital sign patterns  
- Patient-level aggregation of longitudinal measurements  
- Exploratory data analysis (EDA)  

This reflects real-world clinical data science workflows used in healthcare analytics.

---

## Dataset

The dataset is based on a publicly available ICU dataset inspired by the PhysioNet 2019 Sepsis Challenge.

It contains:

- 1,552,210 ICU observations  
- 44 clinical variables  
- Time-series structure (hourly measurements per patient)  
- Patient-level identifiers  
- Binary outcome variable (`SepsisLabel`)

Each row represents a single time-stamped observation per patient in the ICU.

---

## Clinical Variables

### Vital Signs
- Heart Rate (HR)  
- Oxygen Saturation (O2Sat)  
- Blood Pressure (SBP, MAP, DBP)  
- Respiratory Rate (Resp)  
- Temperature (Temp)

### Laboratory Values
- Lactate  
- White Blood Cells (WBC)  
- Creatinine  
- Platelets  
- Glucose  
- pH  
- Bilirubin  
- Electrolytes

### Patient Information
- Age  
- Gender  
- ICU length of stay (ICULOS)  
- Admission time  

---

## Target Variable

- `SepsisLabel`  
  - 0 = No sepsis  
  - 1 = Sepsis

---

## Methodology

### 1. Data Loading & Inspection
- Loading large-scale ICU dataset using Pandas  
- Understanding dataset structure (time-series format)  
- Identifying missing values and data quality issues  

### 2. Data Cleaning & Feature Selection
- Selection of clinically relevant variables  
- Handling missing values  
- Reducing dimensionality for clinical interpretability  

### 3. Patient-Level Aggregation
- Aggregation of hourly ICU data into patient-level features  
- Calculation of mean physiological values per patient  
- Extraction of outcome label per patient  

### 4. Exploratory Data Analysis (EDA)
- Distribution analysis of vital signs  
- Comparison of septic vs non-septic patients  
- Identification of clinical patterns  

### 5. Clinical Interpretation
- Interpretation of lactate, MAP, and HR differences  
- Identification of physiological deterioration patterns  
- Translation of statistical results into clinical insights  

---

## Key Findings

- Patients with sepsis show significantly higher lactate levels  
- Mean arterial pressure (MAP) is lower in septic patients  
- Heart rate is elevated in sepsis cases  
- ICU datasets contain substantial missing laboratory measurements  
- Time-series structure is essential for correct interpretation  

---

## Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

(Optional for dashboard extension: Streamlit / Plotly Dash)

---

## Project Structure
