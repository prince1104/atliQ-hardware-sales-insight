# ATLIQ HARDWARE - SALES INSIGHTS (DATA ANALYSIS AND VISUALIZATION)
### Problem Statement : Atliq Hardware and Peripherals Sales Director is facing issues interms of tracking and knowing their sales insights.

#### Connecting to Data Source, Data Cleaning, Data Transformation, Data Modelling, Data Visualization
#### Skills Used : My SQL, Tableau
Tableau, Mysql, Data Wrangling.
Mysql database has all sales transactions, customers, products and markets information. I have analyse this database and than hook it up with Tableau. In Tableau I perform ETL and data cleaning operations to make it ready so that we can build our dashboard. Then build a powerful dashboard that can help us generate sales insights on Atliq hardware business.

# MYSQL QUERY 
## Sales Insights Data Analysis Project

### Instructions to setup mysql on your local computer

1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer and import

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


# DASHBOARD
![hmmm1111](https://user-images.githubusercontent.com/48179170/134302103-e9648e5e-4762-4655-b7c5-b69a99497e48.png)

