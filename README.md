# HR Insights-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

In modern organizations, employee attrition is a critical metric that directly impacts the stability and efficiency of the workforce. The HR Insight Dashboard aims to address the challenge of understanding and mitigating employee attrition by examining various factors contributing to employees leaving the company. The primary goal is to uncover insights into the reasons behind attrition and identify patterns based on department, age group, gender, and salary range.

Employee attrition, at a rate of 16%, poses challenges to organizational stability, team dynamics, and productivity. The HR Insight Dashboard offers nuanced insights into contributing factors, empowering HR teams to proactively implement targeted strategies for improved employee retention and a more conducive work environment.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in the column "Years with current manager" had some empty data, also the column "Business travel" have some errors that we fixed while woreking on the dataset. 
- Step 5 : A new column was introduced named "Attrition count" using conditional column option, where we took attrition column and gave 1 value for 'yes' and 0 to 'no'.

Snap of new calculated column ,

![Snap](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/ff85ebf8-0c05-43a8-8d65-93722da0c9d0)
