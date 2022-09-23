Begin;
insert into categories(CategoryID,CategoryName,Description) values("9","Personal Hygiene","Oats and vegetables");
Commit;
SAVEPOINT p1;
Begin;
insert into products(ProductID,ProductName,SupplierID,CategoryID,QuantityPerUnit,UnitPrice,UnitsInStock,
UnitsOnOrder,ReorderLevel,Discontinued) values("90","Axe deodrant bodySpray","7","5","250ml","5.5",
"100","0","0","0");
Commit;
savepoint p2;
Begin; 
insert into orders(OrderID,CustomerID,EmployeeID,OrderDate,RequiredDate,ShippedDate,ShipVia,Freight,ShipName,
ShipAddress,ShipCity,ShipPostalCode,ShipCountry) values("10247","COMMI","9","2022-04-10 00:00:00",
"2022-05-09 00:00:00","2022-05-07 00:00:00","3","0.2","reggiani caseifici","Strada Provinciale 124",
"Reggio Emilia","42100","Italy");
Commit;

Begin;
insert into orderdetails(OrderID,ProductID,UnitPrice,Quantity,Discount) values("10247","90","5.25","100","0");
Commit;
