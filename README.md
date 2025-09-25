# Oracle SQL: Customer Sales Query

## Project Overview
This project demonstrates basic SQL skills using Oracle SQL (Oracle Academy environment). The main goal of this query is to extract unique states of customers who made purchases during a specific time period. 

The query joins the `customer` and `sale` tables, filters sales within a specific date range, and returns a sorted list of distinct customer states.

## SQL Query
```sql
SELECT DISTINCT state
FROM customer
JOIN sale
  ON sale.customerid = customer.customerid
WHERE saledate >= DATE '2015-04-01'
  AND saledate <= DATE '2015-05-30'
ORDER BY state;
