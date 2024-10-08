USE hr;
-- 1
SELECT
	first_name,
	last_name
FROM
	employees
WHERE
	department_id IN (80, 90);

-- 2
SELECT
	first_name,
	last_name
FROM
	employees
WHERE
	salary BETWEEN 4999 AND 7001;

-- 3
SELECT
	country_name
FROM
	countries
WHERE
	country_name LIKE '%g%';

-- 4
SELECT
	city
FROM 
	locations
WHERE
	postal_code LIKE '%99' OR postal_code LIKE '99%';
    
-- 5
SELECT
	first_name,
	last_name
FROM
	employees
WHERE
	manager_id IS null;
