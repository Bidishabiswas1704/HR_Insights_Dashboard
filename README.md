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
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various departments, Visual filters (Slicers) were added for three departments named "Human Resource", "Research and Development", & "Sales".

Snap of Visual filters (Slicers),

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/c2ac6f4b-f277-46c0-85e0-88600bd972eb)
- Step 8 : In the report view, under the insert tab, a text boxes was added to the canvas, where name of the Dashboard was mentioned.
- Step 9 : Six card visuals were added to the canvas, one representing Total no. of employees, No. of employees leaving, Employee leaving rate, Average age of employees, Average salary of employee and Average years served at company by the employees leaving it.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.

- Step 10 : A card visual was used to represent the Total no. of employees.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/372ab522-9eba-4091-a4bf-e17c6bc4f966)

Following DAX expression was written for the same,
        
       Total no. of employees  = COUNT(HR_Analytics[EmpID])
- Step 11 : Second card visual was used to represents No. of employees leaving the company.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/196cc87e-115d-4b5d-8589-8ded941f489e)

Following DAX expression was written for the same,
        
       No. of employees leaving  = SUM(HR_Analytics[AttritionCount])
       
- Step 12 : Third card visual was used to represents Employees leaving rate.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/bc385c15-d7a1-4317-a779-c73b2d18addb)
 
Following DAX expression was written for the same,
               
      Employees leaving rate = DIVIDE(SUM(HR_Analytics[AttritionCount]), SUM(HR_Analytics[EmployeeCount]), 0)
      
- Step 13 : Fourth card visual was used to represents Average age of employees leaving the company.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/e34da94d-9f9f-4ab6-984b-a8c441f9b2aa)

Following DAX expression was written for the same,
        
       Employees average age  = AVERAGE(HR_Analytics[AgeGroup])
- Step 14 : Fifth card visual was used to represents Average salary of employees leaving the company.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/84ccb347-e00b-489c-bff8-ca5e6e160844)

Following DAX expression was written for the same,
        
       Employees average salary  = AVERAGE(HR_Analytics[MonthlyIncome])
- Step 15 : Sixth card visual was used to represents Average years served by the employees before leaving the company.

![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/d5b8fff2-ebae-460c-81ef-2e7549032686)

Following DAX expression was written for the same,
        
       Average years served at company  = AVERAGE(HR_Analytics[YearsAtCompany])

- Step 16 : The rest of the report contains a donut chart, two bar charts, two stacked bar charts, one table and an area chart to clearify the problem statement using various visulazation as mentioned.
 - Step 17 : The report was then published to Power BI Service.
 
 
![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/c4fba114-fe06-47f4-b579-ededa2b23ddd)


 # Report Snapshot (Power BI DESKTOP)
 
![image](https://github.com/Bidishabiswas1704/HR_Insights_Dashboard/assets/140384850/24d8f16b-3952-4ee7-9fe7-d8c80669eda3)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;
### [1] Total Number of Employees in the company= 1413

   Number of employees leaving = 229
   
   Employees leaving rate = 16.21 %

   Number of employees leaving (Male) = 145

   Number of employees leaving (Female) = 44

           thus, higher number of employees leaving the company are male.
           
### [2] Average Salary of the Employees leaving the company = 6.5 K

### [3] Average Years by the Employees before leaving the company = 7 yrs
  
  These ratings will change if different visual filters will be applied.  

### [4] Some other insights
 
 ### Attration by Educational Field
 
 1.1) 41% of departing employees hold a background in Life Sciences.
 
 1.2) 311% of departing employees hold a background in Medical fields.
 
 1.3) 11% of departing employees hold a background in Marketing.
 
         thus, maximum employees leaving the company belongs to Life science background..
 
 ### Satisfaction ratings based on Job Roles
 
 2.1)  50/229 employees leaving the company have expressed the lowest satisfaction rating for their respective job roles.
 
 2.2)  62/229 employees leaving the company have expressed the highest satisfaction rating for their respective job roles.
 
         thus, maximum employees leaving the company are satified with their respective job roles.

### Attration by Age
 
3.1)  111 of employees leaving the company belong to 26-35' age group.
 
3.2)  43 of employees leaving the company belong to '18-25' age group.
 
3.3)  41 of employees leaving the company belong to '36-45' age group.
 
3.4)  26 of employees leaving the company belong to '46-55' age group.
 
        thus, most employees leaving the company are young, aged 18-35, seeking varied job experiences and experiments.
         
### Attration by Salary of Employees

4.1) 158 of employees leaving the company have salary range upto 5,000 rs.

4.2) 48 of employees leaving the company have salary range between 5k-10k.
       
       thus, more employees leaving the company have salary less than average salary of the company (6.5k). Thus less salary is the major cause behind employees departing from the company.
       
### No. of years served by Employees before leaving the company

5.1) 57 employees depart the company upon completing their first year of tenure.

5.2) 20 employees depart the company upon completing their five years of tenure.

5.3) 16 employees depart the company upon before completing their first year.


        thus, more after 1st year and 5th year of tenure in the company most of the empoyees depart.

### Attration by Job roles

6.1) Position of "lab technician" sees the highest employee turnover, with 60 individuals departing.

6.2) Position of "Sales Executive" sees the second highest employee turnover, with 55 individuals departing.

6.3) Position of "Research Scientist" sees the third highest employee turnover, with 44 individuals departing.

        thus, job role with the highest employee turnover, accounting for 60 departures, is the Lab Technician position.
