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

'%' all match,
'_' single match
```
