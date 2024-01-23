# SALES-INSIGHTS-ATLIQ-TECHNOLOGIES
INTERACTIVE TABLEAU DASHBOARD WITH REVENUE AND PROFIT ANALYSIS
Tableau Profile Link : https://public.tableau.com/app/profile/sruthy4417/viz/SALESINSIGHTSATLIQHARDWARE/PROFITANALYSIS

# OBJECTIVE :
# DATA ANALYSIS USING SQL

1) To show all customer records

   SELECT * FROM sales.customers;
   
2) Show the total number of customers

   SELECT count(*) FROM sales.customers;

3) Show transactions for the Chennai market (market code for chennai is Mark001)

   SELECT * FROM sales.transactions
   WHERE market_code= 'Mark001';
   
4) Show distinct product codes that were sold in chennai

   SELECT distinct(product_code)
   FROM sales.transactions
   WHERE market_code= "Mark001";

5) Show transactions where the currency is US dollars

   SELECT * FROM sales.transactions
   WHERE currency='USD';

6) Show transactions in 2020 join by date table

   SELECT sales.transactions.*, sales.date.* 
   FROM sales.transactions INNER JOIN sales.date
   ON transactions.order_date=date.date WHERE date.year=2020;

7) Show total revenue in year 2020

   SELECT sum(sales.transactions.sales_amount)
   FROM sales.transactions INNER JOIN sales.date
   ON transactions.order_date=date.date WHERE date.year=2020
   AND sales.transactions.currency = 'INR' or sales.transactions.currency = 'USD';

8) Show total revenue in year 2020, January Month

   SELECT sum(sales.transactions.sales_amount)
   FROM sales.transactions INNER JOIN sales.date
   ON transactions.order_date=date.date WHERE date.year=2020 and date.month_name= "January"
   AND (sales.transactions.currency = 'INR' or sales.transactions.currency = 'USD');

9) Show total revenue in year 2020 in Chennai

    SELECT sum(sales.transactions.sales_amount)
    FROM sales.transactions INNER JOIN sales.date
    ON transactions.order_date = date.date
    WHERE transactions.market_code='Mark001' and date.year='2020';

10) To show the table and alter the column name profit_margin to PROFIT

    DESCRIBE sales.transactions;
    ALTER TABLE sales.transactions
    CHANGE profit_margin PROFIT double

11) To alter the table name profit_margin_percentage to PROFIT_MARGIN

    ALTER TABLE sales.transactions
    CHANGE profit_margin_percentage PROFIT_MARGIN double


![REVENUE ANALYSIS](https://github.com/Sruthyuday/SALES-INSIGHTS-ATLIQ-TECHNOLOGIES/assets/142775795/dea948c2-ab77-4f4e-af2a-1bae9f8b3123)
![PROFIT ANALYSIS](https://github.com/Sruthyuday/SALES-INSIGHTS-ATLIQ-TECHNOLOGIES/assets/142775795/92c6758a-730b-4b96-8996-987180c5f78a)
