# SQLTASK5
✅ Objective
The goal of this task is to practice and demonstrate the use of SQL Joins to combine data from two or more related tables. By the end of this task, you should be comfortable working with INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN to merge data in meaningful ways.
🛠 Tools Required
DB Browser for SQLite

MySQL Workbench


CREATE TABLE Customers (
    customer_id INT PRIMARY KEY,
    name VARCHAR(50),
    city VARCHAR(50)
);

CREATE TABLE Orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    amount INT
);

INSERT INTO Customers VALUES (1, 'lasyaa', 'Hyderabad');
INSERT INTO Customers VALUES (2, 'krishna', 'Mysuru');
INSERT INTO Customers VALUES (3, 'manoj', 'Mumbai');
INSERT INTO Customers VALUES (4, 'Sohan', 'Agra');

INSERT INTO Orders VALUES (101, 1, 5000);
INSERT INTO Orders VALUES (102, 2, 3000);
INSERT INTO Orders VALUES (103, 1, 7000);
INSERT INTO Orders VALUES (104, 5, 2000);

SELECT Customers.name, Orders.amount
FROM Customers
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id;

SELECT Customers.name, Orders.amount
FROM Customers
LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id;

SELECT Customers.name, Orders.amount
FROM Customers
RIGHT JOIN Orders ON Customers.customer_id = Orders.customer_id;

SELECT Customers.name, Orders.amount
FROM Customers
FULL OUTER JOIN Orders ON Customers.customer_id = Orders.customer_id;
