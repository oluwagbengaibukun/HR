# Human Resources Analysis and Dashboard


# Introduction
Human Resource (HR) is equipped with the task of recruiting, employing, compensating employees, developing policies, strategic planning and advice to the organization profit. HR make sure that there is a futuristic approach to every threat / failure that the organization would face. HR is the face of any organization, involved in the day to day running of the activities and ensuring that there’s a smooth running of activities with the thought of covering the loopholes to be faced.There are a lot of activities to be put into place but how can HR explain their multi-tasking approach in a simple form to the organization? This involves reasoning and careful deliberate actions presented in   simple form with the help of Power Bi. Presentation is one of the core processes in data analysis while understanding of the presentation is the main stream of detecting, knowing and putting to action the aims/goals of the organization. There have been a lot of ways to present data but without the ease of understanding and in simple templates, it will need another body of personnel to explain the results. This doesn’t give a good reputation to the information that is being tried to be conveyed. Communication is complete when there is feedback, in which the presentation of data will give value-data on it. Hence, boosting organization performance can be managed by an efficient HR role, overall analysis in benefiting on how retrenched workers affect growth of the status quo is showed.  As a result of discrepancies and inconsistencies discovered in organization after thorough research has been conducted and to further aid the human resource department to be specific and certain with the data they are dealing with, I have decided to come up with more insights using data that penetrate deep into the organization data.  Note that prior to this detailed analysis, an inconclusive information was provided, after which thorough data cleaning was done to achieve the final result.


# Problem Statement
The issue of collating daily report, analyzing employee performance rating, knowing the workers due for promotion and retirement, differentiating permanent and contract staff at each job level, differentiating  the monthly income of the workers by department, contract type, job level and gender and ease in knowing the name of each employee, department type and resource they manage at each level can be limited when being presented with raw data and it would not give room for flexibility of data  inputs. Hence, for any progression in the organization performance, it must involve a coherent work system that can present reports in a simplified format and can be recalled, modified and represented in home-friendly form. The use of Power Bi tackles all this issues but how can the HR make use of it to upgrade their information in giving out profound information in advising the management board on job satisfaction and income rate of the organization?


# Data Sourcing
The Dataset for this project was gotten from Kaggle.  The dataset consisted of two (2) CSV files containing information provided by the organization namely: HR data which contain all details of employees including employee’s number, age, education, job role and level etc., and a separate file which contain employee names.


# Data Cleaning
The first of the dataset is in CSV file in excel which was clustered up in one column
 ![image](https://user-images.githubusercontent.com/51271692/185365480-2945e59d-98d1-4d0b-8bb6-7ab6708fe28a.png)
The file was loaded/imported as Text/CSV to Power BI and then Transform Data to load into power query for cleaning.
![image](https://user-images.githubusercontent.com/51271692/185365831-f2f54633-7921-4ca9-a702-3972ec61db39.png)
then Transform Data to load into power query for cleaning.
![image](https://user-images.githubusercontent.com/51271692/185368023-66321777-d448-4178-9837-fdbac4ed9543.png)
the clustered column was split in power query by clicking split column by delimiter and specifying the delimiter that will be use to split the text column which is: “split at each occurrence of the delimiter” and clicking on the advance options and select columns.
![image](https://user-images.githubusercontent.com/51271692/185369116-b71d5ce8-001e-4225-b42b-56ddd21c8d65.png)
The image below is the resulting state after splitting the columns appropriately 
![image](https://user-images.githubusercontent.com/51271692/185369312-40e46008-3fc4-4d9c-9720-6349691ae205.png)
but note that the column headers are not rightly named, so I cleaned up the column header by “Using First Row as Header” options at the menu bar which auto set the first row as the header
![image](https://user-images.githubusercontent.com/51271692/185369463-f84d2ad6-5a3b-403f-b226-4cd9a5b2bbaf.png)
The table contains 35 columns in total after the split and 1470 rows saved and loaded up to our power BI for analysis and visualization.
![image](https://user-images.githubusercontent.com/51271692/185369847-cca5c90d-4dcf-4476-b5ec-b08ddd2f956f.png)
The second table that contains the employee numbers and names was loaded to power Bi query.
![image](https://user-images.githubusercontent.com/51271692/185369949-30413751-7a7c-48b5-a363-4d07c453f266.png)
And the table is merge with the first table through the common key/attribute which is employee number.
![image](https://user-images.githubusercontent.com/51271692/185370249-79045ae6-ff14-4fd2-8e8c-c3b13ba3c0e3.png)
A new column was generated as shown below as “HR employee data” but the contents are not the employee’s names.
![image](https://user-images.githubusercontent.com/51271692/185370830-3695719f-6102-4463-8d5f-fbe7c166f338.png)
In order to fix this, went to on more option on the newly added column which is HR employee data, deselect the “use original column name as prefix” and deselect the Employee number since the relationship was established on that attribute.
![image](https://user-images.githubusercontent.com/51271692/185370941-87100438-2011-4455-b351-665b4e50eba7.png)
And the column has been fixed with the right content as the employee’s name rather than the table that was earlier capture.
![image](https://user-images.githubusercontent.com/51271692/185371042-e144e928-2ae2-452d-b4dc-0454449d1fbb.png)


# Analysis for Visualization
During the course of analysis and visualization, some columns were added based on the insights we wanted to get from the data such as: Employees due for promotion, employee due retirement/retrenchment, employee contract type. 
For employee that has not been promoted in the last 7 to 15 years are due for promotion. The existing “YearSinceLastPromotion” column was use to get the new column “Promotion”. This was achieved by selecting “YearSinceLastPromotion” column and then using the “Conditional Column” under the “Add Column” menu
![image](https://user-images.githubusercontent.com/51271692/185371767-d74009c8-d9db-400c-87d9-04b431af32eb.png)
Then the Conditional Column setting section is open and the right conditions are put in place
![image](https://user-images.githubusercontent.com/51271692/185374413-fb8c3408-8a95-4bb6-b0d7-ee3f7e946b8f.png)
Below is the resulting image which shows the newly added column Promotion with the appropriate labels hereby increasing the number of columns.
![image](https://user-images.githubusercontent.com/51271692/185374544-0b08ec68-bee5-4def-bb23-e2937ad73302.png)
Retirement status column was added with the same process as the Promotion column but this time, “YearAtCompany” and “Age” columns were used as measures (YearAtCompany was selected before going to the conditional column tab).  The image below shows the measures used to arrive as the Retirement status 
![image](https://user-images.githubusercontent.com/51271692/185374604-7fbfb5a0-e4f4-497e-b0a9-a2136582df44.png)
And here is the resulting Retirement status Column which was use to capture the number of active employees in the organization.
![image](https://user-images.githubusercontent.com/51271692/185374663-7676377b-87a4-4f5f-a366-405fa477bf2f.png)
Contract type column was added with the same process but different measures. Employees in the company are either on contract or permanent bases based on their numbers of years at the company.
![image](https://user-images.githubusercontent.com/51271692/185374773-3fe19921-7192-418a-9a9d-907e97fe16f8.png)
Contract employee are the employee that are less than 2 years   in the company and 2 years above are confirmed as permanent staffs.
![image](https://user-images.githubusercontent.com/51271692/185374888-f313c509-254c-4c63-8e0a-4bddbc0ddbb4.png)
# Data Analysis
Dax Measures 
In order to analysis the data and achieve the desired outcome, a number of Dax measures were created:

1.	Total Employee = DISTINCTCOUNT('HR Analytics Data'[EmployeeNumber]): use to count  the total   number of employee
2.	Male = CALCULATE([Total Employee],'HR Analytics Data'[Gender]= "male") : use to capture the number of male employees
3.	Female = CALCULATE([Total Employee],'HR Analytics Data'[Gender]= "female") : use to capture the number of female employees
4.	%Male = DIVIDE([Male],[Total Employee],0): to get the percentage of the male employee
5.	%Female = DIVIDE([Female],[Total Employee],0): to get the percentage of the female  employee
6.	Due for promotion = CALCULATE([Total Employee],'HR Analytics Data'[Promotion]="Due for promotion"): to capture the number of employee due for promotion
7.	%Due for promotion = DIVIDE([Due for promotion],[Total Employee],0): to get the percentage of the employee due for promotion
8.	Not Due = CALCULATE([Total Employee],'HR Analytics Data'[Promotion]="Not yet due") : to capture the number of employee not yet due for promotion
9.	Active Workers = CALCULATE([Total Employee],'HR Analytics Data'[Retirement Status]="Not due for retirement"): to capture the number of active employees
10.	AttritionYes = CALCULATE([Total Employee],'HR Analytics Data'[Attrition]="Yes"): to capture the number of employee that has left the company
11.	%AttritionYes = DIVIDE([AttritionYes],[Total Employee],0): to capture the number of employee that has left the company in percentage
12.	AttritionNo = CALCULATE([Total Employee],'HR Analytics Data'[Attrition]="No"): to capture the number of employee that are still active in the company 
13.	%AttritionNo = DIVIDE([AttritionNo],[Total Employee])*100: to capture the number of employee that are still active in the company in percentage
14.	Contract = CALCULATE([Total Employee],'HR Analytics Data'[Contract type]= "Contract"): to capture  the number  of employee on contract bases. 
15.	Permanent = CALCULATE([Total Employee],'HR Analytics Data'[Contract type]= "Permanent"): to capture  the number  of employee on permanent bases.


# Visualization
This project visualization was done with Power BI. It is a five (5) page dashboard with each pages holding different insights and also a navigation buttons section to help navigate from one page to another. 
![image](https://user-images.githubusercontent.com/51271692/185375209-139026c9-22f2-429c-93b9-7b69239fa1de.png)
![image](https://user-images.githubusercontent.com/51271692/185375240-cb33ce59-42d3-48e0-befb-4531886ef23c.png)
![image](https://user-images.githubusercontent.com/51271692/185375267-be3f09c6-2cda-4248-8d6f-7ce9518c3d22.png)
![image](https://user-images.githubusercontent.com/51271692/185375285-79284f16-ad3e-4f75-946c-51e96bf1fc7a.png)
![image](https://user-images.githubusercontent.com/51271692/185375308-cb0a8f4b-2bdb-491d-9413-3f956c3ff689.png)


#  Key Insights from the Analysis
1.	The number and name of employee due for promotion
2.	The number and names of employee due for retirement due to age or number of years in service 
3.	The attrition rate of the company
4.	The performing department in term of monthly income
5.	The performance rating and job satisfaction rating of each Job roles and departments.
6.	The contract type performance.

Note:  More insights can still be explored with the dataset but this work was done based on insights request from the HR department of the company.


# Recommendations
1.	Employee that has work or function in a single post/position for 5years and above should be promoted based on their performance rating 
2.	Incentives should be provided for the contract employees so as to boast their performance.
3.	The company should set retirement age and also number of maximum years an employee can use in service.
4.	The HR should work more with the employee to beat down the attrition rate of the company.



