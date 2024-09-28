# Tietokannat Ohjelmisto 1

# Relaatiotietokannan peruskäsitteiden harjoitukset

![ruudunkaappaus](1-1.png)

# Tietokannan suunnittelu harjoitukset

![ruudunkaappaus](2-1.png)

# Yhteen tauluun kohdistuvien kyselyiden harjoitukset

### Tehtävä 1

SELECT * FROM goal
![ruudunkaappaus](3-1.png)

### Tehtävä 2

SELECT * name FROM airport WHERE iso_country = "FI"
![ruudunkaappaus](3-2.png)

### Tehtävä 3

SELECT name FROM airport WHERE iso_country="FI" ORDER BY name ASC
![ruudunkaappaus](3-3.png)

### Tehtävä 4

SELECT name, type FROM airport WHERE iso_country="FI" ORDER BY type, name 

![ruudunkaappaus](3-4.png)

### Tehtävä 5

SELECT name FROM country WHERE name like "F%"

![ruudunkaappaus](3-5.png)

### Tehtävä 6

SELECT name FROM country WHERE name like "%f%"

![ruudunkaappaus](3-6.png)

### Tehtävä 7

select location from game where screen_name = "Vesa"

![ruudunkaappaus](3-7.png)

### Tehtävä 8

select co2_consumed from game where screen_name = "Ilkka"
![ruudunkaappaus](3-8.png)

### Tehtävä 9

select distinct co2_budget From game
![ruudunkaappaus](3-9.png)

# Where-osan liitosehto harjoitukset

### Tehtävä 1

select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";

![ruudunkaappaus](4-1.png)

### Tehtävä 2