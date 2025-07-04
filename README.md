# DIGITAL SKILLUP ACADEMY (DSA) CAPSTONE DATA ANALYSIS PROJECT 

### Palmora Group HR Analysis

## Overview
This project is a case study completed as part of my Data Analysis learning journey. The analysis was conducted using Microsoft Power BI, focusing on gender inequality on isssues like gender pay gap across departments in Palmoria group.

# Dataset Description
The dataset contains Palmoria HR data gotten from the CHRO, Mr Yunus Shofoluwe

# HR Details: Gender, department, salary, location, rating and bonus rules

Data Size: 946 rows, 11 columns

# Steps Taken to clean the dataset

I started by using **countblank function** to determine the number of blanks that needed to be filled.
I proceeded to fill them with the required information.
The next step was to import the data into my power bu environment and used the transform data function to work on the dataset. I removed the **null** for the columns where they appeared because they had no use. I ensured to use “keep top rows” function to keep the nulls from returning before clicking on close and apply.
I re-launched the file and also imported the second file that also needs to be transformed and then clicked on transform data. 
I unpivoted the table except the department column in order to establish a relationship between the datasets. I proceeded to create a “custom column” and named it Dept Rating.
I merged the queries as new.
Next, I created another custom column in order to formulate “annual bonus”.
In order to show the pay distribution of employees, I created a conditional column to show the band of salary and to know the number of employees receiving the minimum salary of 90,000.
Finally I clicked on close and apply.

 ##  Analysis Tasksk Codes & Key Insights

Using **Microsoft Power BI, Custom Columns, and conditional formatting**, I performed the following analysis:
# 1.	Gender Distribution Analysis 
Measures Used
Gender Count = COUNT('Employee'[Gender])
Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))`

# 2.	Minimum Salary Requirement Analysis
Measures used
 Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])

# 3.	Rating insights based on gender
Measures used
Average rating by Gender = AVERAGE('Employee'[Rating])`
Rating Count by gender = COUNT('Employee'[Rating])`

# 4.	Salary Structure and Gender Pay Gap Analysis
Measure used
Average Salary by Gender = AVERAGE('Employee'[Salary])`
Salary Count by Department and Region = COUNT('Employee'[Salary])`

##  Files Included

- `Palmoria _HR_Analysis.pbix`: Power BI file with cleaned data and analysis
- `Charts.png`: Key visualizations used to support findings
- `README.md`: Project overview (this file)

---

##  Tools Used

- Microsoft Power BI 
  - Custom Columns  
  - Conditional Formatting   
  - Charts & Graphs
