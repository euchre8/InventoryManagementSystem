#                                            INTRODUCTION
In this world, at this time, we have a ubiquitous and essential entity called database management
system. It is a software used to manage databases. Database management has evolved from a
specialized computer application to a central component of a modern computing environment,
and, as a result, knowledge about database systems has become an essential part of an education
in computer science.
The project INVENTORY MANAGEMENT SYSTEM is an example of working database system
where we manage inventory and analyze the day-to-day records of a dairy. 



# LIST OF ABBREVIATIONS
    IMS Inventory Management System
    
    DBMS Database Management System
    
    DDL Data Definition Language
    
    DML Data Manipulation Language
    
    SQL Structured Query Language
    
    SSMS SQL Server Management Studio Express
    
    ER Entity Relationship


# FUNCTIONALITIES
    Total Sales 
  Date wise, Product wise, Week wise, Month wise, Previous Months Data,
            
    Variance
  Day wise, Week wise, Month wise --- All in graphs

    Products
  Milk, Ghee – 2 types, Curd, Nasika, Ark – 3 types, Phenyl, Mustard Oil
 
    Customer Orders
  In order to see the seasonal effect in sale we need to trace out orders from customers for our products, though it can be tracked     with sales also.

    Product Wise Sales
  Target vs Actual, Profit vs Loss, Monthly

    Auto message
  If loss is more than 5% in each product and cumulative sales.
   
    Capital Items Tracing
  Purchase date and Total amount, Depreciation, etc.

    Connectivity with customers
  As soon as we are launching new products or stores.
 
    Tracking
  Tracking down the customer feedback and suggestions.
  
# Entity Relationship Diagram
    NORMALIZED DATABASE SCHEMA
Following is the database schema after passing through the normalization stages:
1NF – First Normalized Form, 2NF – Second Normalized Form, 3NF – Third Normalized Form, BCNF – Boyce-Codd Normalized Form

The final schema

[https://github.com/prasadankit33/StockManagement/blob/master/dfd.JPG]

# RELATIONAL ALGEBRA OPERATIONS INCORPORATED
++ PROJECT (π)
++ CARTESIAN PRODUCT (A X B)
++ JOIN ( )
++ UNION (∪)
++ INTERSECTION (∩)

# DDL QUERIES INCORPORATED
++ CREATE DATABASE
CREATE DATABASE INVENTORY

++ CREATE TABLE
  CREATE TABLE customer (
  Cid INT NOT NULL,
  Cname VARCHAR(20) NOT NULL,
  ContactNo INT,
  EmailId VARCHAR(20),
  PRIMARY KEY(Cid)
  )

++ ALTER TABLE
    ALTER TABLE productinvoice
    ADD CONSTRAINT productinvoice_PInvNo_FK FOREIGN KEY(PInvNo) REFERENCES
    purchasedby(PinvNo)



# DML QUERIES INCORPORATED
   
    INSERT INTO
 INSERT INTO customer VALUES (2, 'Rick Sanchez', 9983646163, 'ricksan@gmail.com');

    SELECT
  SELECT Cname, SInvNo, Amount
  FROM customer, sellsto
  WHERE customer.Cid = sellsto.cid


# ADVANCED SQL FEATURES INCORPORATED
  
    TRIGGER
  A trigger is executed when a new product is added an email is sent to the customers to
  notify them.
  If loss is more than five percent a trigger is executed to inform the admin.
