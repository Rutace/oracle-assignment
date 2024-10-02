INSERT INTO Customers (Name, Email) VALUES ('Alice', 'alice@example.com');
INSERT INTO Customers (Name, Email) VALUES ('Bob', 'bob@example.com');

INSERT INTO Orders (CustomerID, OrderDate, TotalAmount) VALUES (1, '2024-08-01', 150.00);
INSERT INTO Orders (CustomerID, OrderDate, TotalAmount) VALUES (2, '2024-08-02', 200.00);

INSERT INTO Products (Name, Price) VALUES ('Widget A', 10.00);
INSERT INTO Products (Name, Price) VALUES ('Widget B', 15.00);

SELECT Customers.Name, Orders.OrderDate
FROM Customers
JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

SELECT Orders.OrderID, Products.Name, Products.Price
FROM Orders
JOIN Products ON Orders.OrderID = Products.OrderID;
