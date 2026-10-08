# Week 4 SQL Assignment — Advanced SQL Aggregations

## Database Used

classicmodels

## Question 1

Write an SQL query to show the total payment amount for each payment date from the payments table.

* Display payment date and total amount paid on that date.
* Sort payment date in descending order.
* Show only the top 5 latest payment dates.

### SQL Query

```sql
SELECT paymentDate, SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;
```

## Question 2

Write an SQL query to find the average credit limit of each customer from the customers table.

* Display customer name, country, and average credit limit.
* Group by customer name and country.

### SQL Query

```sql
SELECT customerName, country, AVG(creditLimit) AS average_credit_limit
FROM customers
GROUP BY customerName, country;
```

## Question 3

Write an SQL query to find the total price of products ordered from the orderdetails table.

* Display product code, quantity ordered, and total price for each product.
* Group by product code and quantity ordered.

### SQL Query

```sql
SELECT productCode,
       quantityOrdered,
       SUM(quantityOrdered * priceEach) AS total_price
FROM orderdetails
GROUP BY productCode, quantityOrdered;
```

## Question 4

Write an SQL query to find the highest payment amount for each check number from the payments table.

* Display check number and highest amount.
* Group by check number.

### SQL Query

```sql
SELECT checkNumber,
       MAX(amount) AS highest_amount
FROM payments
GROUP BY checkNumber;
```

## Conclusion

The assignment demonstrates the use of SQL aggregate functions including SUM(), AVG(), and MAX(), together with GROUP BY, ORDER BY, and LIMIT clauses using the classicmodels database.
