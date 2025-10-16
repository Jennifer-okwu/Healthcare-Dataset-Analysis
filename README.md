# Healthcare-Dataset-Analysis-2019-2024
Using Power BI, I generated key insights from the synthetic healthcare dataset designed to reflect real-world medical data. By analyzing the dataset, we seek to derive insights that will help stakeholders understand patient demographics, admission patterns, medical conditions, billing and test results.

## Project Topic: Healthcare Dataset Analysis (2019-2024) – Multi Category Classification Problem

### Project Overview

This data analysis aims to apply my Power BI skills in generating key insights from the synthetic healthcare dataset designed to reflect real-world medical data. By analyzing the dataset, we seek to derive insights that will help stakeholders understand patient demographics, admission patterns, medical conditions, billing and test results. And also derive actionable recommendations that can influence healthcare planning, resource allocation, and billing strategies.

### Table of Contents

### Data Sources

The primary source of data used is healthcare_dataset.csv which was downloaded from Kaggle. The dataset contains multiple patient-level attributes (demographics, admissions, billing, medications, test results). [Download Here](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)

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

