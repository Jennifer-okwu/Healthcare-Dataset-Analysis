# Healthcare-Dataset-Analysis
Using Power BI, I generated key insights from the synthetic healthcare dataset designed to reflect real-world medical data. By analyzing the dataset, I seek to derive insights that will help stakeholders understand patient demographics, admission patterns, medical conditions, billing and test results.

## Project Topic: Healthcare Dataset Analysis (2019-2024) – Multi Category Classification Problem

### Project Overview

This data analysis aims to apply my Power BI skills in generating key insights from the synthetic healthcare dataset designed to reflect real-world medical data. By analyzing the dataset, we seek to derive insights that will help stakeholders understand patient demographics, admission patterns, medical conditions, billing and test results. And also derive actionable recommendations that can influence healthcare planning, resource allocation, and billing strategies.

### Table of Contents

### Data Sources

The primary source of data used is healthcare_dataset.csv which was downloaded from Kaggle. The dataset contains multiple patient-level attributes (demographics, admissions, billing, medications, test results). [Download Data](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)

### Tools Used

Microsoft Power BI – Employed for creating interactive and visually appealing reports [Download Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

### Data Cleaning and Preparation

The following was performed during the data cleaning and preparation phase;
- Data loading and inspection
    - Data was imported and taken to the power query editor for transformation.
- Data cleaning and formatting
    - Capitalized each word in the name column.
    - Replaced the value “UnitedHealthcare” in Insurance Provider column with “United Healthcare”.
    - Added Conditional column for age groups: Below 18 (Children), 18-39 (Youths), 40-64 (Middle age) and 65 and above (Elderly).
    - Sorted the age groups in ascending order using the conditional column named “Age Sort”.
    - Changed data type.

 ### Project Structure – Exploratory Data Analysis

EDA involved the exploration of the data to answer questions and derive insights from the data.

### Data Analysis

Some of the DAX expressions used during the analysis are:
``` DAX
Total Number of Records = COUNTROWS (healthcare_dataset)

```
``` DAX
Gender Count = COUNT (healthcare_dataset [Gender])

```

``` DAX
Sum of Billing Amount = SUM(healthcare_dataset [Billing Amount])

```

``` DAX
Average Billing Amount = AVERAGE(healthcare_dataset[Billing Amount])

```

### Result/ Findings

The following insights were derived from the analysis;
- Males are 0.08% more than females in the overall gender distribution. The dataset has fewer of its population as children (below 18yrs) and most of its population are within 40-64yrs.

![Healthcare 1](https://github.com/user-attachments/assets/ef3c60c3-e682-4eb0-951b-3362ce73cd95)

- Elective and Urgent admission types had the highest population of patients. More males were admitted through the urgent admission type and more females were admitted via elective admission. More emergency admissions were recorded among patients below 18 years. More urgent admissions were recorded among patients 40-64yrs and 65yrs and above. 
- Cigna insurance covered most urgent and emergency admissions while United Healthcare insurance covered most elective admissions. While Abbott hospitals had the least number of admissions, LLC Smith had the highest number of admissions.

![Healthcare 2](https://github.com/user-attachments/assets/a2b1c5a2-d3bd-4802-805e-4c1ca3de7d9d)

- There is a high prevalence of obesity in patients below 18yrs. Diabetes is more prevalent in patients between 40-64yrs. Arthritis and Cancer is more prevalent in patients 18-39yrs and Asthma is more prevalent in patients above 64yrs of age.
- All 5 medications were prescribed across all medical conditions with Lipitor being the overall most prescribed drug and also the most prescribed medication in urgent admission. Aspirin was prescribed more for females and in elective admission while Paracetamol was prescribed more for males and in emergency admission. Aspirin and Penicillin was observed to be prescribed more for patients in the middle age and elderly age groups.

![Healthcare 3](https://github.com/user-attachments/assets/47f80782-39bc-4668-a92e-f37e3a949875)

- The overall dataset showed more abnormal test results especially in urgent admission, arthritis condition and in patients below 18yrs and 40-64ys. Inconclusive test results were prevalent in urgent and emergency admissions and in hypertensive medical conditions.
- There was a sustained spike in the number of test results generated in 2020 (which is probably due to the COVID-19 outbreak) all through till 2023, then a sharp decline in 2024.
Johnson PLC generated the most inconclusive test results. LLC Smith, Ltd Smith and Smith PLC hospitals generated the most abnormal results.

![Healthcare 4](https://github.com/user-attachments/assets/3ff3830c-9eca-4542-89b4-de7619ff68b7)

- Cigna Insurance covered most of the bill of over #287m. Johnson PLC had the highest billing amount of over #1m. Some hospitals were discovered to be in debt. Elective and Urgent admissions were had the highest billing amounts.

![Healthcare 5](https://github.com/user-attachments/assets/6bc0d7c5-0aa4-4134-89d8-68498820e7ce)

### Recommendations

- Community healthcare awareness outreaches should be organized to educate the public on the causes, risk-factors and prevention of prevalent medical conditions.
- Create a consistent and standardized admission process in hospitals to improve efficiency and reduce variability.
- Patients should be allowed to complete information electronically and provide necessary details before their arrival to speed up the in-person check-in process.
- Staff training should be prioritized to maintain an effective admission of patients.
- Pre-test preparation should be optimized to prevent test sample issues and inaccurate test results.
- Correct procedures for handling test samples should be followed to ensure accurate results.
- Re-testing or trying different test methods for inconclusive test results.
- Hospitals should implement diagnostic excellence programs by creating multi-disciplinary teams including laboratory and radiology experts to improve test use and reduce errors.	

### Limitations

The dataset lacks a unique identifier e.g. Patient ID. I discovered that some names were shared by more than one patient with completely different records. This can easily be mistaken duplicates in the record without the unique identifier.
