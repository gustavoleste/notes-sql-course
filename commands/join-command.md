# JOIN COMMAND

## EXAMPLES

```sql
SELECT colunm(s)
FROM left_table_name
(INNER | RIGHT | LEFT | FULL) JOIN right_table_name
ON condition(s)
WHERE condition(s)
ORDER BY _value;
```

```sql
SELECT *
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id
```
```sql
SELECT martian.martian_id, base.base_id, base.base_name
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id;
```
```sql
SELECT m.martian_id, b.base_id, b.base_name
FROM martian AS m
INNER JOIN base AS b
ON m.base_id = b.base_id;
```
```sql
SELECT v.first_name AS visitor_fn, v.last_name AS visitor_ln,
m.first_name AS martian_fn, m.last_name AS martian_ln
FROM visitor AS v
LEFT JOIN martian AS m
ON v.host_id = m.martian_id;
```
```sql
SELECT m.first_name AS fn, m.last_name AS ln,
s.first_name AS super_fn, s.last_name AS super_ln
FROM martian AS m
LEFT JOIN martian AS s
ON m.super_id = s.martian_id
ORDER BY m.martian_id;
```
```sql
SELECT s.supply_id,i.quantity,s.name,s.description
FROM (SELECT * FROM inventory WHERE base_id = 1) AS i
RIGHT JOIN supply AS s
ON i.supply_id = s.supply_id
ORDER BY s.supply_id;
```
```sql
SELECT v.first_name AS visitor_fn,v.last_name AS visitor_ln,
m.first_name AS martian_fn, m.last_name AS martian_ln
FROM visitor AS v
FULL JOIN martian AS m
ON v.host_id = m.martian_id
WHERE m.martian_id IS NULL OR v.sisitor_id IS NULL;
```