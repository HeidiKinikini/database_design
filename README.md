#Computer Company Database Design

## Overview
This project is a relational database design created for a simulated computer company. The goal was to model core business operations such as customer records, product inventory, and service-related data in a structured SQL database.

## Purpose
The database was designed to support common business needs, including:
- tracking customers and their orders
- managing inventory and product details
- organizing employee or service records
- maintaining relationships between key business entitites

## Project Structure 

- ERD.jpg -- Entity Relationship Diagram of the database
- dbDesigns.png -- Additional database design visuals
- computer_company_database.accdb -- Microsoft Access database file
- README.md -- Project documnetation

## Database Structure
This project includes tables related to answer questions such as: 
-Customers
-Products / Inventory
-Orders
-Employees
-Service or support records

## Example Use Cases
Example queries can be used to answer questions such as:
- Which customers placed recent orders?
- What products are currently in inventory?
- Which services were performed for a given customer?
- How are orders connected to products and customers?

## What I learned
Through this project, I practiced:
- designing relational databases
- defining table relationships
- using primary and foreign keys
- applying normalization concepts
- writing SQL queries based on business requirements

## Notes
This project was developed as a part of a database design exercise using a simulated company scenario. It is included here as a portfolio example of database modeling and SQL fundamentals.

## Future Imporvements
- add more advanced reporting queries
- improve indexing strategy
- expand support for service ticket tracking
- build a simple frontend to interact with the database

## Security Considerations
While this project focuses on database design, secure database practices are important, including:

- enforcing proper access controls
- preventing unauthorized data access
- ensuring data integrity through constraints
- minimizing risk of SQL injection through proper query handling

Future improvements could include implementing role-based access and auditing.

## Example Queries

The following queries demonstrate how the database can be used to retrieve and analyze business data: 

```sql
-- Retrieve all customers
SELECT * FROM Customers;

--Get all orders placed by a specific customer
SELECT * FROM Orders
WHERE CustomerID = 1;

-- Find products currently in stock
SELECT * FROM Products
WHERE Quantity > 0;

-- Join customers with their orders
SELECT Customers.Name, Orders.OrderDate
FROM Customers
JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

-- View order details with product information
SELECT Orders.OrderID, Products.ProductName, OrderDetails.Quantity
FROM OrderDetails
JOIN Products ON OrderDetails.ProductID = Products.ProductID
JOIN Orders ON OrderDetails.OrderID = Orders.OrderID;
