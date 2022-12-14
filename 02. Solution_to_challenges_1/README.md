 Here we are going to explore some typical business situation challenges. We are starting from the fundamental statements such as:

- ```SELECT```
- ```SELECT DISTINCT```
- ```COUNT```
- ```ORDER BY```
- ```LIMIT```
- ```LIKE```

## Q1. How many payment transactions were greater than $5.00?

```sql
SELECT 
COUNT(amount) 
FROM payment
WHERE amount > 5;
```

*Output:*

|count|
|:---:|
|3618 |


## Q2. How many actors have a first name that starts with the letter P?

```sql
SELECT 
COUNT(*) 
FROM actor
WHERE first_name 
LIKE 'P%';
```

*Output:*

|count|
|:---:|
|  5  |


## Q3. How many unique districts are our customers from?

```sql
SELECT 
COUNT(DISTINCT(district)) 
FROM address;
```

*Output:*

|count|
|:---:|
| 378 |


## Q4. Retrieve the list of names for those distinct districts from the previous question.

```sql
SELECT 
DISTINCT(district) 
FROM address
LIMIT 10;
```

*Output:*


|     District    |
|:---------------:|
|Aden             |
|Eastern Visayas  |
|Vaduz            |
|Tokat            |
|Anzotegui        |
|Saint-Denis      |
|Chollanam        |
|Chihuahua        |
|Nyanza           |
|Changhwa         |


## Q5. How many films have a rating of R and a replacement cost between $5 and $15?

```sql
SELECT 
COUNT(*) 
FROM film
WHERE rating = 'R'
AND replacement_cost 
BETWEEN 5 AND 15;
```

*Output:*

|count|
|:---:|
|  52 |


## Q6. How many films have the word Truman somewhere in the title?

```sql
SELECT 
COUNT(*) 
FROM film
WHERE title 
LIKE '%Truman%';
```

*Output:*

|count|
|:---:|
|  5  |

