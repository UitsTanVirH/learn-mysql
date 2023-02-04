# learn-mysql

# In operator 
```
SELECT *
FROM sql_store.customers
WHERE state Not IN ('VA' , 'FL', 'MA')
```
# Between operator
```
SELECT *
FROM sql_store.customers
WHERE points between 1000 and 3000
```
# Like operator
```
SELECT * 
FROM sql_store.customers
where last_name like '%b%'

SELECT * 
FROM sql_store.customers
where last_name like '_____y'

'%' any number of characters,
'_' single characters
```
# Null operator
```
SELECT * 
FROM sql_store.orders
where shipper_id is null
```
# Limit clause
```
SELECT * 
FROM sql_store.customers
limit 5

SELECT * 
FROM sql_store.customers
limit 5, 3 
(5 is offset here, skips the first 5 rows and shows after that)
```
# Joins

# Inner joins
```
select o.order_id, c.first_name, c.last_name
from orders as o
join customers as c
	on o.customer_id = c.customer_id
```
