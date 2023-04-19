# Employee_Attrition_Prediction
## Overview 
   - Analyze employee's charactistics who left or stayed in the company.
   - Use machine learning to build models and check model performance on predictions. 

## DataSource
   [Human_Resources.csv](https://github.com/CelineWW/Employee_Attrition_Prediction/blob/main/Human_Resources.csv)
   - This is a clean dataset, including 1470 employees information without unkown or missing value.
   - 35 Columns: 
      - 7 object columns: ***Attrition, BusinessTravel, Department, EducationField, Gender, JobRole, MaritalStatus***
      - 28 number columns: ***Age, DailyRate, DistanceFromHome, Education, EmployeeCount, EmployeeNumber, EnvironmentSatisfaction, HourlyRate, JobInvolvement, JobLevel, JobSatisfaction, MonthlyIncome, MonthlyRate, NumCompaniesWorked, Over18, OverTime, PercentSalaryHike, PerformanceRating, RelationshipSatisfaction, StandardHours, StockOptionLevel, TotalWorkingYears, TrainingTimesLastYear, WorkLifeBalance, YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager***
   
## Results
### Data Preprocessing
   - Use lambda function to convert boolen columns to numerical data.
      ```
      employee_df['Attrition'] = employee_df['Attrition'].apply(lambda x:1 if x == 'Yes' else 0)
      employee_df['OverTime'] = employee_df['OverTime'].apply(lambda x:1 if x == 'Yes' else 0)
      employee_df['Over18'] = employee_df['Over18'].apply(lambda x:1 if x == 'Y' else 0)
      ```
   - Use histogram to check distributions of each column
   ![hist1](https://user-images.githubusercontent.com/105877888/233159024-cf27cc13-8bba-4933-861b-34b56d7ec0cb.png)
   ![hist2](https://user-images.githubusercontent.com/105877888/233159087-ed33fdbd-8398-4b30-96f8-704bcebe775d.png)

   
   Over18 Y
   OverTime
   StandardHours 80
   EmployeeCount 1
   Attrition label

## Summary
