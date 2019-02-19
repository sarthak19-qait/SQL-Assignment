# SQL-Assignment

# 1
SELECT customerName,checkNumber,paymentDate,amount 
FROM customers
JOIN payments
WHERE customers.customerNumber = 1001;

# 2
SELECT employeeNumber, lastName, firstName, reportsTo
FROM employees
WHERE reportsTo = 1001 ;

# 3
SELECT customerName, phone, SUM(payments.amount)
FROM customers
JOIN payments
ON customers.customerNumber = payments.customerNumber
WHERE creditLimit > 10000 
GROUP BY payments.amount;

# 4
SELECT orderdetails.orderNumber, orders.orderDate, products.productCode, orderdetails.quantityOrdered, products.buyPrice
FROM orders
INNER JOIN orderdetails ON orders.orderNumber = orderdetails.orderNumber 
INNER JOIN products on orderdetails.productCode = products.productCode
WHERE orders.customerNumber = 103;


