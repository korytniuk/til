# Execution order example

e.g.

```
SELECT *
FROM <condition>
WHERE <condition>
GROUP BY <condition>
HAVING <condition>
ORDER BY <condition>
LIMIT
```

on the server side will execute in the order:

```
FROM (it selects the table that is required)
WHERE (it filters the rows based on condition)
GROUP BY (it aggregates the result that was filtered)
HAVING (additional level of filtering for aggregated values)
SELECT (it selects the appropriate columns from the result)
ORDER BY (it arranges values in ascending or descending order)
LIMIT (it controls how many rows are outputted in the query)
```

