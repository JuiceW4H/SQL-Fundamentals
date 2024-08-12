# SQLBolt-Ortega

SQL Review

1. List all the Canadian cities and their populations
```
Command: SELECT Country, Population FROM north_american_cities WHERE Country="Canada";
```
<br>

2. Order all the cities in the United States by their latitude from north to south
```
Command: SELECT * FROM North_american_cities WHERE Country = "United States" ORDER BY Latitude DESC;
```
<br>

3. List all the cities west of Chicago, ordered from west to east
```
Command: SELECT City FROM North_american_cities WHERE Longitude < -87.629798 ORDER BY Longitude ASC;
```
<br>
  
4. List the two largest cities in Mexico (by population)
```
Command: SELECT * FROM North_american_cities WHERE Country = "Mexico" ORDER BY Population DESC LIMIT 2;
```
<br>
  
5. List the third and fourth largest cities (by population) in the United States and their population
```
Command: SELECT City, Population FROM North_american_cities WHERE Country="United States" ORDER BY Population DESC LIMIT 2 OFFSET 2;
```
<br>

SQL Lesson 12

1. Find the number of movies each director has directed
```
Command: SELECT Director, COUNT() FROM Movies LEFT JOIN Boxoffice ON Movies.id = Boxoffice.movie_id GROUP BY Director;
```
<br>

2. Find the total domestic and international sales that can be attributed to each director
```
Command: SELECT Director, SUM(Domestic_sales) + SUM(International_sales) as Total FROM Movies LEFT JOIN Boxoffice ON Movies.id = Boxoffice.movie_id GROUP BY Director;
```
<br>

SQLPD Activity

Case 1: A hacked site members' details have surfaced on a darknet forum. Please submit all members' details.
```
SELECT * FROM members;
```
<br>

Case 2: A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries given names and number of promotions sent' details.
```
SELECT GivenName, Promotions FROM mailing_list;
```
<br>

Case 3: An illegal site's servers were seized in a recent operation. Please submit all users emails, number of posts and last names' details.
```
SELECT Email, Posts, LastName FROM users;
```
<br>

Case 4: An illegal site's servers were seized in a recent operation. Please submit all users given names' details.
```
SELECT DISTINCT GivenName FROM users;
```
<br>
Please make sure there are no duplicates.

Case 5: An illegal site's servers were seized in a recent operation. Please submit all users' details sorted by given names in ascending order.
```
SELECT * FROM users ORDER BY GivenName ASC;
```
<br>

Case 6: White hat hacker has sent SQLPD exposed members' details of a shady site connected to various persons of interest. Please submit all members' details sorted by names in descending order.
```
SELECT * FROM members ORDER BY Name DESC;
```
<br>

Case 7: A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries number of kids, emails and join dates' details sorted by join dates in descending order. Please make sure there are no duplicates.
```
SELECT DISTINCT NumberOfKids, Email, JoinDate FROM mailing_list ORDER BY JoinDate DESC;
```
<br>

Case 8: An illegal site's servers were seized in a recent operation. Please submit all users surnames, access times and emails' details sorted by access times in ascending order and then by surnames in descending order.
```
SELECT Surname, AccessTime, Email FROM users ORDER BY AccessTime ASC, Surname DESC;
```
<br>

Case 9: White hat hacker has sent SQLPD exposed subscribers' details of a shady site connected to various persons of interest. Please submit the top 20 subscribers' details when sorted by full names in ascending order and then by password hashes in ascending order.
```
SELECT * FROM subscribers ORDER BY FullName ASC, PasswordHash ASC LIMIT 20; |
```
<br>

Case 10: A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit the top 20 records surnames, given names and number of password changes' details when sorted by number of password changes in descending order and then by given names in descending order. Please make sure there are no duplicates.
```
SELECT DISTINCT Surname, GivenName, PassChangeCount FROM mailing_list ORDER BY PassChangeCount DESC, GivenName DESC LIMIT 20;
```
<br>
