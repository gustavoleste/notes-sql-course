# SELECT COMMAND

## EXAMPLES:
```sql
SELECT colunm_name, colunm_name
FROM table_name 
WHERE condition_01 (AND | OR) condition_02
ORDER BY colunm_name (ASC | DESC)
LIMIT number;
```

```sql
SELECT * FROM earthquake;
```
```sql
SELECT COUNT(*) FROM earthquake;
```

```sql
SELECT magnitude,place,occurred_on 
FROM earthquake;
```

```sql
SELECT * 
FROM earthquake 
WHERE occurred_on >= '2000-01-01';
```

```sql
SELECT * 
FROM earthquake 
WHERE occurred_on >= '2000-01-01' AND occurred_on <= '2010-12-31'
ORDER BY magnitude DESC
LIMIT 1;
```
```sql
SELECT MIN(occurred_on), MAX(occurred_on)
FROM earthquake;
```

```sql
SELECT DISTINCT cause
FROM earthquake;
```

```sql
SELECT COUNT(*)
FROM earthquake
WHERE cause = 'earthquake';
```

```sql
SELECT COUNT(*)
FROM earthquake
WHERE place LIKE '%Honshu%Japan%'
AND occurred_on BETWEEN '2011-03-11' AND '2011-03-18'
```
```sql
SELECT SUM(salary)
FROM secret_table
```
```sql
SELECT year_released, ROUND(AVG(tempo))
FROM songs
GROUP BY year_released
ORDER BY year_released;
```