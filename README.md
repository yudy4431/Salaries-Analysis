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
2. 


