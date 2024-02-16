# Salaries-Analysis
In this case, we use GCP and MySQL Workbench to build ETL process. Then utilize Python to analyze the details.
This project includes three parts:
1. Exploring data by Python, including data manipulating, mining, and visualizing.
2. GCP building and MySQL database connecting.
3. MySQL quries to find out insights of questions.


## Table of Content
1. Introduction
2. About Dataset
3. Exploring Data Set
4. GCP and MySQL Workbench Builing
5. MySQL Quires for insights
   

## 1. Introduction
This dataset provides comprehensive insights into salary trends and factors influencing compensation within the data industry.
In this dataset, we can analyze salary trends over the years and across different job categories within the data industry. For instance, we can plot the median salary for Data Scientists, Data Engineers, and Data Analysts over the years to identify any noticeable trends. Additionally, we can compare the salary distribution between different experience levels within each job category to understand how experience influences compensation.


## 2.About Dataset
Variables description: https://www.kaggle.com/datasets/hummaamqaasim/jobs-in-data/data  
### There are 13 variables and 9355 rows in the dataset, with no any NaN values.  


<img width="488" alt="Screenshot 2024-02-16 at 11 48 24" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/c0e54562-a1ef-4db3-91df-401ff592c231"></br>

<img width="385" alt="Screenshot 2024-02-16 at 11 56 41" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/8c0ccb87-3815-42f2-a3ec-dd2d61ad8793">


### Descriptive


<img width="449" alt="Screenshot 2024-02-16 at 11 57 11" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/6e92a1fe-6b11-4770-99c7-c04e95299b67"> </br>

<img width="330" alt="Screenshot 2024-02-16 at 11 57 00" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/f39a71fa-54ae-42af-bfd6-adaf688be82a">


## 3. Exploring Dataset


### Check duplicated data and manipulate.
There are duplicated rows, after we remove them, we have 5341 rows left.  


<img width="500" alt="Screenshot 2024-02-16 at 12 02 38" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/0a7e220b-d55b-43e7-aa20-60a13c0f9258"> </br>
<img width="435" alt="Screenshot 2024-02-16 at 12 04 27" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/d7d5e7e4-1245-438d-840f-fab2ef4a0559">


### Most frequency of each column.
We can know that most people are in Data Science field as a Data Engineer.  
Most of the people are Senior level, and work type is In-person.
This is a bit more than expected because the data period is 2020-2023, and we assumed that Remote would be the most popular mode of work, but the data tells us that In-person is still in the majority.  
<img width="1099" alt="Screenshot 2024-02-16 at 12 05 46" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/59a82013-e489-4956-98fc-540d1f860787">


### Analysis by Work Year
The graph shows that the number of employed people rises with the number of years.
![work year](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/658f1d2b-18e2-4da2-912d-1484c1b2fc0f)


### Analysis by Job Title and Salaries
Data Scientis and Data Engineer are the most two pupular job title with higher salaries than other positions.
![job title](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/c606fc45-912e-4bf6-937f-7790edf32a81)


### Analysis by Job Category
The market needed more Data field talent than others.
![category](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/cf4aa222-a789-47c5-b4e4-cb14a6e8495d)



### Analysis of Job Category in Each Year
Jobs have an increasing trend.
![cat2023](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/8ae52d8f-93c6-4d8e-9daf-2e23f65748fd)</br>
![cat2022](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/10c2635e-7a0f-45d1-a708-7f4a36b694c4)</br>
![cat2021](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/060423e1-f4ba-4845-81ca-b9dc38425c9e)</br>
![cat2020](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/d55ef69d-4d3d-40ef-aa2c-524dad4f8101)


### Analysis of Mean Salary in USD in each year
We can see that the position related to AI has become a big part and have higher salaries.
![mean2023](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/3cb9f73a-22d4-479c-b40c-ad291b5906f4)</br>
![mean2022](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/10be74ef-1ece-49c5-ab7d-fc3db874d6e5)</br>
![mean2021](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/4afd2521-9ba1-4bdd-943e-772c0c422325)</br>
![mean2020](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/a41fb81d-d5b7-4f15-8da9-d5c0cc4c2eb6)


### Analysis of Work Type
The job market needed more Senior level positions.
![experience](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/ce4e9eb2-5790-4c03-b1f4-dd50d4207017)



### Analysis of Work Type
In-person position accounts for the biggest part, but Remote work setting is close.
![work setting](https://github.com/yudy4431/Salaries-Analysis/assets/73131672/ac4d72c9-d067-45ce-9f04-223a18997611)




## 4. Google Cloud Platform Database Setting
Create a GCP bucket. In order to save the management cost of the cloud system, the number of vCPU is set to 1, the amount of memory is set to 3.75GB, and the storage mode is changed from SSD to HDD according to the usage pattern and amount of database.

<img width="620" alt="setting" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/2e6c2531-d6e8-458a-8847-58d2c64a4c8f">


### Set connection to public and get IP address for MySQL Workbench use
<img width="682" alt="connection" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/f3ee8842-32d0-4510-a052-2b96d84c50b1">


### Config network setting for GCP instance, GCP SQL, and MySQL Workbench


1. Create a database in MySQL Workbench.

```create database 'stem_salary';```


2. Create Table: stem

```
USE stem_salary;
CREATE table stem(
id int(10),
work_year int(6),
job_title varchar (50),
job_category varchar(50),
salary_currency varchar(10),
salary int(10),
salary_in_usd int(10),
employee_residence varchar(50),
experience_level varchar(50),
employment_type varchar(50),
work_setting varchar(50),
company_location varchar(50),
company_size varchar(300),
);
```


### Use GCP to import data

1. Import data to Cloud Storage.
<img width="675" alt="cloud" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/d2f95fd6-9651-4cbd-963c-851ffd887c0e">


2. Upload CSV file into GCP SQL.
<img width="871" alt="import" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/2a16db41-3da4-4172-ada4-92ccb727043b">


### Now can use MySQL Workbench to query.
<img width="614" alt="SQL" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/8be96e39-a6cc-42a7-91dd-6d8a583a0e84">


# Exploring data by Python (salaries.ipynb)






