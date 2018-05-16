CREATE TABLE Person ( ID INTEGER PRIMARY KEY AUTOINCREMENT, Name string, Age integer, Height integer, City string, FavoriteColor string )

INSERT INTO Person( Name, Age, Height, City, FavoriteColor ) VALUES ('Adam Dreier', 24, 190, 'Commack', 'Blue');
INSERT INTO Person( Name, Age, Height, City, FavoriteColor ) VALUES ('Barbara Dreier', 59 , 170, 'Commack', 'Purple');
INSERT INTO Person( Name, Age, Height, City, FavoriteColor ) VALUES ('Edward Dreier', 59 , 160, 'Commack', 'Blue');
INSERT INTO Person( Name, Age, Height, City, FavoriteColor ) VALUES ('Joe Dreier', 22 , 190, 'Commack', 'Green');
INSERT INTO Person( Name, Age, Height, City, FavoriteColor ) VALUES ('Baylie Dreier', 20 , 160, 'Commack', 'Pink');

SELECT * FROM Person ORDER BY Height DESC

SELECT * FROM Person ORDER BY Height ASC

SELECT * FROM Person ORDER BY Age DESC

SELECT * FROM Person WHERE Age > 20

SELECT * FROM Person WHERE Age < 20 OR Age > 30

SELECT * FROM Person WHERE Age <> 27

SELECT * FROM Person WHERE FavoriteColor <> 'Red';

SELECT * FROM Person WHERE FavoriteColor <> 'Red' AND FavoriteColor <> 'Blue';

SELECT * FROM Person WHERE FavoriteColor = 'Orange' OR FavoriteColor = 'Green';

SELECT * FROM Person WHERE FavoriteColor IN('Orange','Green','Blue');

SELECT * FROM Person WHERE FavoriteColor IN('Yellow','Purple');

==============================================================================

CREATE TABLE Orders ( PersonID integer, ProductName string, ProductPrice float, Quantity integer );

INSERT INTO Orders ( PersonID, ProductName, ProductPrice, Quantity) VALUES (1, 'Coke', 1.15, 10)
NSERT INTO Orders ( PersonID, ProductName, ProductPrice, Quantity) VALUES (4, 'Pepsi', 1.75, 16)
NSERT INTO Orders ( PersonID, ProductName, ProductPrice, Quantity) VALUES (4, 'Barqs', 1.25, 14)
NSERT INTO Orders ( PersonID, ProductName, ProductPrice, Quantity) VALUES (4, 'Sprite', 1.05, 112)
NSERT INTO Orders ( PersonID, ProductName, ProductPrice, Quantity) VALUES (4, 'Tab', 1.25, 5)

SELECT * FROM orders;

SELECT SUM(Quantity) FROM Orders;

SELECT SUM(ProductPrice * Quantity) FROM Orders;

SELECT SUM(ProductPrice * Quantity) FROM Orders WHERE PersonID = 1;

==============================================================================
INSERT INTO Artist ( Name ) VALUES ( 'VanGough' );
INSERT INTO Artist ( Name ) VALUES ( 'Picasso' );
INSERT INTO Artist ( Name ) VALUES ( 'DaVinci' );

SELECT * FROM Artist ORDER BY Name DESC LIMIT 10;

SELECT * FROM Artist ORDER BY Name ASC LIMIT 5;

SELECT * FROM Artist WHERE Name LIKE 'Black%';

SELECT * FROM Artist WHERE Name LIKE '%Black%';

==============================================================================

SELECT FirstName, LastName FROM Employee WHERE City ='Calgary';

SELECT FirstName, LastName, Max(BirthDate) FROM Employee;

SELECT FirstName, LastName, Min(BirthDate) FROM Employee;

SELECT * FROM Employee WHERE ReportsTo = 2;

SELECT COUNT (*) FROM Employee WHERE City = 'Lethbridge';

==============================================================================

SELECT Count (*) FROM Invoice WHERE BillingCountry = 'USA';

SELECT Max(Total) FROM Invoice;

SELECT Min(Total) FROM Invoice;

SELECT * FROM Invoice WHERE Total > 5;

SELECT COUNT (*) FROM Invoice WHERE Total < 5;

SELECT COUNT (*) FROM Invoice WHERE BillingState IN ('CA','TX','AZ');

SELECT AVG(Total) FROM Invoice;

SELECT SUM(Total) FROM Invoice;

