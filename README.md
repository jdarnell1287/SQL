# SQL
SQL Portfolio

CREATE TABLE Specialty_Products (id INTEGER PRIMARY KEY, item TEXT, price INTEGER, stock_level INTEGER, weekly_sale_average INTEGER);

insert into Specialty_Products values 
(1, 'Gluten-free Bread Flour', 6.99, 12, 9), 
(2, 'Gluten-free Oyster Sauce', 3.49, 5, 5),
(3, 'Gluten-free Pancake Mix', 4.99, 10, 6),
(4, 'Coconut Aminos', 3.29, 6, 3),
(5, 'Vegan Cheese', 4.59, 9, 7),
(6, 'Soy Chorizo', 2.99, 3, 3),
(7, 'Macadamia Milk Ice Cream', 8.99, 2, 3),
(8, 'Grain-free Granola', 6.79, 5, 7),
(9, 'Chickpea Flour Penne', 3.99, 3, 3),
(10, 'Chickpea Flour Elbows', 3.99, 5, 2),
(11, 'Chickpea Flour Tortellini', 3.99, 2, 3);

CREATE TABLE Local_Vendor_Products (id INTEGER PRIMARY KEY, item TEXT, price INTEGER, stock_level INTEGER, weekly_sale_average INTEGER);

insert into Local_Vendor_Products values
(1, 'Local Wildflower Honey', 15.99, 1, 3),
(2, 'Local Pasture_Raised Eggs', 4.79, 12, 9),
(3, 'Assorted Microgreens', 5.79, 8, 12),
(4, 'Hollow Brewery IPA', 12.99, 10, 6),
(5, 'Local Goat Cheese', 6.89, 4, 7);

select * from specialty_products order by price asc;

select * from local_vendor_products where stock_level > 4 order by
stock_level asc;

select sum (stock_level) from specialty_products;
select sum (stock_level) from local_vendor_products;
