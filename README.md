# SQLBolt-Ortega

1. List all the Canadian cities and their populations
Command: SELECT Country, Population FROM north_american_cities WHERE Country="Canada";

2. Order all the cities in the United States by their latitude from north to south
Command: SELECT * FROM North_american_cities WHERE Country = "United States" ORDER BY Latitude DESC;

3. List all the cities west of Chicago, ordered from west to east
Command: SELECT City FROM North_american_cities WHERE Longitude < -87.629798 ORDER BY Longitude ASC;

4. List the two largest cities in Mexico (by population)
Command: SELECT * FROM North_american_cities WHERE Country = "Mexico" ORDER BY Population DESC LIMIT 2;

5. List the third and fourth largest cities (by population) in the United States and their population
Command: SELECT City, Population FROM North_american_cities WHERE Country="United States" ORDER BY Population DESC LIMIT 2 OFFSET 2;
