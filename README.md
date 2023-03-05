## Sales Insights Data Analysis Project

### Instructions to setup mysql on your local computer

1. SQL database dump is in sales_db_dump.sql file above.

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distinct product codes that were sold in Chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

See sales_insights_BI.pdf for final look of dashboard.

#### Analysis for the year 2020:-

-> Sales are steadily declining in the last four months(Mar-Jun).

-> Bhuwaneswar has more profit margin even though Delhi has more sales.

-> Mumbai is contributing 23.9% of all the profit.

-> Delhi is providing only 22.1% profit.

-> Although Delhi is the biggest market in terms of revenue , Mumbai is the top contributor in terms of profit by market.

-> Excel Stores, Surge Stores and Electricalsara Stores contribute the most profit (36.3%).

-> Electricalsara Stores has the highest revenue contribution(46.2%) with just 0.4% profit margin.



#### To increase profit, following points maybe considered :

Product Quality

Promotion/Advertising

Discounts

Healthy communication between management/suppliers

Product packaging

Identify which areas product to be sold.


#### To increase the sales growth, following points can be studied:

-Revenue by zone

-Sales qty by zone-Revenue trend

-Revenue by markets

-Sales qty by markets

-Top 5 customer by revenue

-Top 5 products by revenue

-Last 4 year revenue(by zone and by overall sales)

-Identify customer providing less revenue

-Identify customer providing top revenue

-Identify markets having less sales (bottom 5)

-Identify the product where revenue is increasing by zone,markey and customer





