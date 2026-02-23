# Healthcare Workforce Mental Health Analysis

### This repository contains SQL-based analytical project built on top of the *Healthcare Workforce Mental Health Dataset*.
---

## Dataset
This analysis uses the dataset originally provided by **River Wilkinson** on Kaggle:
##### Healthcare Workforce Mental Health Dataset:
Source: https://www.kaggle.com/datasets/rivalytics/healthcare-workforce-mental-health-dataset?select=Dataset+Overview+-+Healthcare+Workforce+Mental+Health.pdf

Original dataset license: **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**
You are free to use and adapt the dataset as long as you provide proper attribution and share derivative data under the same license.

## About this Dataset
Columns, data types and short description of each field:

Column | Data type | Description
---|---|---
employee_id | NVARCHAR |
employee_type | NVARCHAR | 
department | NVARCHAR | 
workplace_factor | NVARCHAR | 
stress_level | NUMERIC | 
burnout_frequency | NVARCHAR | 
job_satisfaction | NUMERIC | 
access_to_eaps | NVARCHAR | 
mental_health_absences | NUMERIC | 
turnover_intention | NVARCHAR | 

## About the project


## Getting started

### Requirements
* SQL engine (I used SQL Server Management Studio 22 in this project)
* Access to dataset CSV file
  
### Instructions
1. Download the dataset from Kaggle.
2. Create new database in SSMS.
3. Run the SQL script as shown below (remember to update the commented-out sections):

```sql
DROP TABLE IF EXISTS --Healthcare--;

GO

CREATE TABLE --Healthcare-- (
employee_id            NVARCHAR(50),
employee_type          NVARCHAR(50),
department             NVARCHAR(50),
workplace_factor       NVARCHAR(50),
stress_level           NUMERIC,
burnout_frequency      NVARCHAR(50),
job_satisfaction       NUMERIC,
access_to_eaps         NVARCHAR(50),
mental_health_absences NUMERIC,
turnover_intention     NVARCHAR(50)
);

GO

BULK INSERT --Healthcare--
FROM --'C:\Users\dkosm\Desktop\archive\Healthcare Workforce Mental Health Dataset.csv'--
WITH (
FIRSTROW = 2,
FIELDTERMINATOR = ',',
TABLOCK);
```
---
## Key Insights

## Licensing

### Code
The code in this repository is licensed under the MIT License.

### Dataset and Derived Data
The dataset and any transformed data files in this repository are made available under the **CC BY-SA 4.0 License**, in accordance with the original dataset terms.
You must provide appropriate attribution and distribute any derivative data under the same license.
