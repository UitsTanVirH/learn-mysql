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
# Self join
```
SELECT e.employee_id, e.first_name, e.last_name, em.first_name as Manager
from employees e
join employees em
	on e.reports_to = em.employee_id
```
# Joining mulitiple table
```
SELECT p.date, c.client_id as Client_Id, c.name as Client, p.amount, pm.name as Method
from clients as c
join payments as p
	on c.client_id = p.client_id
join payment_methods as pm 
	on p.payment_method = pm.payment_method_id
```
# Outer join
	# Left join
```
SELECT 
    c.customer_id,
    c.first_name,
    o.order_id
from customers as c
left join orders as o
    on c.customer_id = o.customer_id
order by c.customer_id

(Returns all the fields from left table)
```
	# Right join
