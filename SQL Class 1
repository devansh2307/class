1) Find name, address and status of bike stations that are still active

SELECT name,address,status
FROM `bigquery-public-data.austin_bikeshare.bikeshare_stations`
where status = "active"
limit 10

 https://drive.google.com/file/d/1WzN6pmLmYOvrA_TYLfAbDBb1amToK2_k/view?usp=sharing


2) Find the number of countries with country code ending with letter 'A'.

SELECT Count(country_name) as no_of_countries FROM `bigquery-public-data.country_codes.country_codes`
where alpha_2_code like '%A' 

https://drive.google.com/file/d/1fvqR_ZyfqEt406_pLLoiudmXkeFihAOM/view?usp=sharing

 

3) Find states and counties with hospital beds greater than or equal to 500 and order them in ascending order.

SELECT state_name, county_name, total_hospital_beds FROM `bigquery-public-data.covid19_aha.hospital_beds` 
where total_hospital_beds >= 500
Order by state_name ASC
LIMIT 1000

https://drive.google.com/file/d/1_NUIPJh8v7w21ivYpDh0rpgj_dEIxC7j/view?usp=sharing

4) Find the states whose name starts with letter "M" having greater than or equal to 500 beds. 

SELECT * 
FROM `bigquery-public-data.covid19_aha.hospital_beds` x
Inner Join `bigquery-public-data.covid19_aha.staffing` y 
on x.county_fips_code= y.county_fips_code 
where y.state_name like 'M%' 
and x.total_hospital_beds >=500

https://drive.google.com/file/d/1Ifhl-QK0EPFFC6hVvLYGglPpc4cwvzUc/view?usp=sharing

5)Group the states with their respective total number of beds available. The states to be taken must have total beds greater than or equal to 500 beds.
SELECT state_name, sum(total_hospital_beds) as total_beds 
FROM `bigquery-public-data.covid19_aha.hospital_beds`
group by state_name
having total_beds >500 
order by total_beds asc
LIMIT 1000

https://drive.google.com/file/d/16M0DNDdjMyt9MIX4o4LBsVS29pcsnFEC/view?usp=sharing

6)
SELECT year,primary_type, count(*) 
FROM `bigquery-public-data.chicago_crime.crime` 
where primary_type= 'ROBBERY'and year BETWEEN 2019 AND 2023
group by year, primary_type 

https://drive.google.com/file/d/1DSgPh0XwxQP0oAO5Zk9Q7R6EaLjL-Mwt/view?usp=sharing

7
SELECT primary_type, count(*) AS frequency 
FROM `bigquery-public-data.chicago_crime.crime` 
group by primary_type
Order by frequency desc

https://drive.google.com/file/d/1pj47Z9xnfn0SKG_sijPYFLurGGSaP6Dl/view?usp=sharing

8
SELECT y.state_name, sum(x.total_hospital_beds) as total_beds,sum(y.total_nursing_home_personnel_ft) as total_nurses 
FROM `bigquery-public-data.covid19_aha.hospital_beds` x
Right Join `bigquery-public-data.covid19_aha.staffing` y 
on x.county_fips_code= y.county_fips_code 
group by y.state_name
order by total_beds Desc, total_nurses desc

https://drive.google.com/file/d/1edC18Rj6E_L_U_6MkJM4Yrk1V-N0puZ6/view?usp=sharing

9)
SELECT x.state_name, x.total_hospital_beds, y.total_personnel_ft
FROM `bigquery-public-data.covid19_aha.hospital_beds` x
Right Join `bigquery-public-data.covid19_aha.staffing` y on x.county_fips_code= y.county_fips_code 
WHERE x.total_hospital_beds IS NULL OR y.total_personnel_ft IS NULL

https://drive.google.com/file/d/1iNff9dx7k9pUM1aCX-DbzXPAKLosQ-UZ/view?usp=sharing

10) SELECT state_name,avg(num_airborne_infection_isolation_rooms) as airborne 
FROM `bigquery-public-data.covid19_aha.hospital_beds` 
group by state_name

https://drive.google.com/file/d/1hvLY9GQdNXL6vJ-BZZS_mso8xOYtiT5T/view?usp=sharing

