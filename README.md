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

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
![REVENUE ANALYSIS](https://github.com/Sruthyuday/SALES-INSIGHTS-ATLIQ-TECHNOLOGIES/assets/142775795/dea948c2-ab77-4f4e-af2a-1bae9f8b3123)
![PROFIT ANALYSIS](https://github.com/Sruthyuday/SALES-INSIGHTS-ATLIQ-TECHNOLOGIES/assets/142775795/92c6758a-730b-4b96-8996-987180c5f78a)
