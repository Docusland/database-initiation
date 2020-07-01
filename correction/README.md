# Question 1
```sql
Select ContactName from Customers
```
--> 91 enregistrements

# Question 2
```sql 
SELECT * from PRODUCTS WHERE CategoryID = 1
```
--> 12 enregistrements

# Question 3
```sql
Select Products.ProductName, Categories.CategoryName, Suppliers.SupplierName
from Products, Categories, Suppliers
WHERE Products.SupplierID = Suppliers.SupplierID
AND Products.CategoryID = Categories.CategoryID
```
--> 77 enregistrements

# Question 4
```sql
SELECT Categories.CategoryName, count(OrderDetails.OrderDetailID) as "Nb Order Details", sum(OrderDetails.Quantity*Products.Price) as "Sum Order Cost"
FROM Categories, OrderDetails, Products
WHERE Categories.CategoryID = Products.CategoryID
AND Products.ProductID = OrderDetails.ProductID
Group by Categories.CategoryName
```

# Question 5
```sql
CREATE TABLE utilisateur
(
    id INT PRIMARY KEY NOT NULL,
    nom VARCHAR(100),
    prenom VARCHAR(100),
    email VARCHAR(255),
    date_naissance DATE,
    pays VARCHAR(255),
    ville VARCHAR(255),
    code_postal VARCHAR(5),
    nombre_achat INT
)
```
# Question 6
Il s'agit du principe de cardinalité. Nous pourrions par exemple mettre le code postal et la ville dans une autre table. Et les pays encore dans une troisieme table. 

