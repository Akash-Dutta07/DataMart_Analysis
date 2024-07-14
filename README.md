# DataMart_Analysis

![images](https://github.com/user-attachments/assets/d99610f1-528b-46aa-927d-db8fa955d198)


## 📄 **OBJECTIVE**
Data Mart is the latest venture, and assistance is needed to analyze its sales and performance. In June 2020, large-scale supply changes were implemented at Data Mart, ensuring all products now use sustainable packaging methods at every step, from the farm to the customer. Assistance is required to quantify the impact of this change on the overall sales performance for Data Mart and its separate business areas.





**SCHEMA USED** : WEEKLY_SALES_TABLES


  

| Column_Name | Data_Type   | 
| :-------- | :------- | 
| week_date | Date 
region | varchar(20)
platform | varchar(20)
segment | varchar(10)
customer | varchar(20)
Transactions | Int
Sales | Int


##  📥 **DATA SOURCING & DATA CLEANING**
The SQL-Script is provided in this repository.
Download and **RUN** The SQL-Script to get the Tables. After, which the following Data_Cleaning activities are performed to clean the Data for smooth Analysis

**A. Data Cleansing Steps**
In a single query, perform the following operations and generate a new table in the data_mart schema named clean_weekly_sales:
 1. Add a week_number as the second column for each week_date value, for example any value from the 1st of January to 7th of January will be 1, 8th to 14th will be 2, etc. 

2. Add a month_number with the calendar month for each week_date value as the 3rd column 

3. Add a calendar_year column as the 4th column containing either 2018, 2019 or 2020 values 

4. Add a new column called age_band after the original segment column using the following mapping on the number inside the segment value
 
 ![Screenshot (29)](https://github.com/user-attachments/assets/da651c3d-98d5-4b72-8e8f-6f1b9466becb)
 
 5. Add a new demographic column using the following mapping for the first letter in the segment values:

 
![Screenshot (30)](https://github.com/user-attachments/assets/74376746-beae-4fbc-aadd-6f7efd87abe1)

6. Ensure all null string values with an "unknown" string value in the original segment column as well as the new age_band and demographic columns 

7. Generate a new avg_transaction column as the sales value divided by transactions rounded to 2 decimal places for each record
  
## 📄**Data Exploration**


1. How many total transactions were there for each year in the dataset? 

2. What are the total sales for each region for each month? 

3. What is the total count of transactions for each platform 

4. What is the percentage of sales for Retail vs Shopify for each month? 

5. What is the percentage of sales by demographic for each year in the dataset? 

6. Which age_band and demographic values contribute the most to Retail sales?

  Findings from all the above analyses are provided in the attached PDF---Datamart(codes)
## 📝 **CONCLUSION**
By examining Data Mart's data, users can make informed purchasing decisions and discover new product preferences. They can gain insights into trending categories and popular products, as well as receive personalized recommendations tailored to their tastes. Identifying the most purchased items and top-selling brands helps users find popular products and spot emerging trends. This analysis engages customers by offering fresh and relevant shopping experiences. Ultimately, these data insights enhance customer satisfaction, boost Data Mart's reputation, and drive revenue growth through increased customer engagement and retention.
