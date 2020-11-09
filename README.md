# Pewett-Hackard-Analysis

## Overview of Project
This report summarizes the analysis done for the Pewett-Hackard company on their employee database.  we used PostgreSQL to perform SQL queries on the data to determine likely retirements and readiness of the organization to train and fill roles that will be left vacant by the retiring employees.

## Results

### Analysis of Retiring Employees
In our analysis we took the employees and titles tables to determine the employees likely to retire.  We used the years 1952 to 1955 as the criteria for determining employees likely to retire.  Linking these 2 tables we were able to provide a list of likely retiring employees by title.  However, the list had duplicate names as some employees as shown in the table below.

![image_name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/retirement_titles.PNG)

To overcome the duplicate employee name issue we created another table using the DISTINCT ON SQL function to filter the names to include only the most recent title.  Please see updated table below

![image name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/unique_titles.PNG)

From this table we created a summary table that gives the count of retiring employees for each title as shown below.

![image name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/retiring_titles.PNG)

### Analysis of Employees Eligible for the Mentorship Program.

For the second part of our analysis we ran a query to determine which employees are eligible for a mentorship program to replace the retiring employees.  The criteria was employees born in 1965.  To gather this data we queried the employees table, department employee table and titles table to pull employees names, birth dates, employment dates and titles.  filtering the table on birth dates in 1965.  the table is shown below.
![image name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/mentorship_eligibility.PNG)

### Summary of Conclusions and Further Analysis
* The greatest needs are for Senior Engineers and Senior Staff.
* The Manager position is the least needed position to fill.
* We needed a summary of the Employees Eligible for the mentorship program to compare to the retiring employees.  We created an addition query taking a count of the mentorship eligible employees by title.  Please see summary table below. 
* From the table below we can see that there is an acute shortage of engineers and managers to mentor into the needed senior positions.

![image name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/mentoring_titles.PNG)

*
*
*
*
![image name](https://github.com/jbates2549/Pewett-Hackard-Analysis/blob/main/combined_title.PNG)
