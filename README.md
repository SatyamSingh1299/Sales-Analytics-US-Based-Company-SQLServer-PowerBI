<h1 align="center">Sales Analytics - Data Analysis using Power BI & SQL Server <a /href="https://public.tableau.com/app/profile/satyam.singh7169/vizzes" target="_blank" rel="noreferrer">

### Project Description
- Performed analytics on a US-based hardware company with branches all over the country.  
- Developed ETL mappings using SQL Server to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design a star schema data model on Power BI.  
- Developed a Power BI dashboard to perform analysis, producing quantitative visualisations in Power BI to draw valuable insights based on different parameters affecting the company's performance year on year and further provide business solutions.

## Technologies    
* Advance Excel  
* SQL Server 
* Power BI/Tableau  
* Statistics  

## Problem Statement
The sales director wants to know the company's performance in various states & accordingly provide discounts.  

- Q1. Revenue breakdown by cities.  
- Q2. Revenue breakdown by years & months.  
- Q3. Top 5 customers by revenue & sales quantity.  
- Q4. Top 5 Products by revenue.    
- Q5. Net Profit & Profit Margin by Market  

## Approach  
  
##### 1. Purpose
To unlock sales insights that may not be known yet and can help in decision-making for respective stakeholders.  

##### 2. Stakeholders  
- Sales Director, 
- I.T. Team 
- Customer Service Team   
- Data & Analytics Team.

#### 3. Goal  
An automated dashboard providing quick & latest sales insights to support data-driven decision making.

#### 4. Measure  
- Dashboards uncovering sales order insights with the latest data available.
- The sales team can make better decisions & prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually to save 20% of their business time & reinvest it in value-added activity.

### Data Flow  
<p  align="center"><img width="80%" src="https://github.com/SatyamSingh1299/Sales-Analytics-US-Based-Company-SQLServer-PowerBI/blob/main/images/flow.jpg" /></a></p>

### Setup  
  
Step 1: Download file: **db_dump.sql** or **db_dump.xlsx**.  
Step 2: Import it in SQL Server and perform ETL(Extract, Transform, Load) if required.  
Step 3: Download Power BI.  
Step 4: Connect Power BI with SQL Server database or Excel database.  
Step 5: Save the file as **pbix**.  
  
## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

2. Show the total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for the Houston market (market code for Houston is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distinct product codes that were sold in Houston.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 joined by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in the year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="USD\r";`
	
8. Show total revenue in the year 2020, January.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and transactions.currency="USD\r";`

9. Show the total revenue in the year 2020 in Houston.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Data Analysis Using Power BI 
  
#### Creating a Star Schema in Power BI
	
<p  align="center"><img width="80%" src="https://github.com/SatyamSingh1299/Sales-Analytics-US-Based-Company-SQLServer-PowerBI/blob/main/images/schemaPowerBI.png" /></a></p>

#### Power BI Dashboard  
	
<p  align="center"><img width="100%" src="https://github.com/SatyamSingh1299/Sales-Analytics-US-Based-Company-SQLServer-PowerBI/blob/main/images/Dashboard_PBI.png" /></a></p>  

<p  align="center"><img width="100%" src="https://github.com/SatyamSingh1299/Sales-Analytics-US-Based-Company-SQLServer-PowerBI/blob/main/images/Dashboard_PBI2.png" /></a></p>

  
## Project References: 🔗

1. https://github.com/mrankitgupta/Sales-Insights-Data-Analysis-using-Tableau-and-SQL?tab=readme-ov-file#data-analysis-using-sql
  
