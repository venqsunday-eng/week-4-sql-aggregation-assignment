# Week 4 SQL Assignment — Advanced SQL Aggregations

## Database Used
classicmodels

## Question 1
Write an SQL query to show the total payment amount for each payment date from the payments table.

- Display payment date and total amount paid on that date.
- Sort payment date in descending order.
- Show only the top 5 latest payment dates.

### SQL Query
```sql
SELECT paymentDate, SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;
