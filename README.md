# Salaries-Analysis
In this case, we use GCP and MySQL Workbench to build ETL process. Then utilize Python to analyze the details.

## Google Cloud Platform Database Setting
Create a GCP bucket. In order to save the management cost of the cloud system, the number of vCPU is set to 1, the amount of memory is set to 3.75GB, and the storage mode is changed from SSD to HDD according to the usage pattern and amount of database.

<img width="620" alt="setting" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/2e6c2531-d6e8-458a-8847-58d2c64a4c8f">

## Set connection to public and get IP address for MySQL Workbench use
<img width="682" alt="connection" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/f3ee8842-32d0-4510-a052-2b96d84c50b1">

## Config network setting for GCP instance, GCP SQL, and MySQL Workbench

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

## Use GCP to import data

1. Import data to Cloud Storage.
<img width="675" alt="cloud" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/d2f95fd6-9651-4cbd-963c-851ffd887c0e">

2. Upload CSV file into GCP SQL.
<img width="871" alt="import" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/2a16db41-3da4-4172-ada4-92ccb727043b">

## Now can use MySQL Workbench to query.
<img width="614" alt="SQL" src="https://github.com/yudy4431/Salaries-Analysis/assets/73131672/8be96e39-a6cc-42a7-91dd-6d8a583a0e84">



