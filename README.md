# assignment15.2


create table if not exists olympics
(
athlete string,
age int,
country string,
year int,
closing_date date,
sports string,
gold int,
silver int, 
bronze int,
total int
)
row format delimited
fields terminated by ',';

SELECT country,count(*) FROM olympics where sports = 'swimming' GROUP BY country;
SELECT year,count(*) FROM olympics where country = 'india' GROUP BY year;
SELECT country,count(*) FROM olympics GROUP BY country;
SELECT country,count(*) FROM olympics where gold >= 0 GROUP BY country;
