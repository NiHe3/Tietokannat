# Tietokannat Ohjelmisto 1

# Relaatiotietokannan peruskäsitteiden harjoitukset

![ruudunkaappaus](1-1.png)

# Tietokannan suunnittelu harjoitukset

![ruudunkaappaus](2.1.png)

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

select airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport"

![ruudunkaappaus](4-2.png) 

### Tehtävä 3

select country.name as "country_name", airport.name as "airport_name"
from airport, country
where country.continent like 'AN' AND airport.iso_country like country.iso_country 

![ruudunkaappaus](4-3.png) 


### Tehtävä 4

Select elevation_ft
From airport, game
where game.screen_name like 'Heini' and game.location like airport.ident

![ruudunkaappaus](4-4.png) 


### Tehtävä 5

SELECT (elevation_ft * 0.3048) AS elevation_m
FROM airport, game
WHERE game.screen_name LIKE 'Heini' AND game.location LIKE airport.ident;

![ruudunkaappaus](4-5.png)  

### Tehtävä 6

SELECT name 
FROM airport, game
WHERE game.screen_name LIKE 'Ilkka' AND game.location LIKE airport.ident

![ruudunkaappaus](4-6.png)  

### Tehtävä 7

Select country.name as "name"
From country, airport, game
where game.screen_name = "Ilkka" and game.location = airport.ident and airport.iso_country = country.iso_country 

![ruudunkaappaus](4-7.png) 


### Tehtävä 8

 
select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";

![ruudunkaappaus](4-8.png) 


### Tehtävä 9 

select airport.name
    from airport, game, goal, goal_reached
    where game.screen_name = "Ilkka" and goal.name = 'CLOUDS' AND game.id = goal_reached.game_id and goal_reached.goal_id = goal.id and game.location = airport.ident


![ruudunkaappaus](4-9.png) 


### Tehtävä 10 


select country.name
     from country, goal, goal_reached, airport, game
    where game.screen_name = "Ilkka" AND goal.name = 'CLOUDS' AND game.id = goal_reached.game_id and goal_reached.goal_id = goal.id and game.location = airport.ident AND airport.iso_country = country.iso_country
    
![ruudunkaappaus](4-10.png) 

