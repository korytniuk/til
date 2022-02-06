# OVER or window functions 

- Window functions do not reduce the number of rows in the output unlike GROUP BY
- They operate on a set of rows and return a single value for each row from the underlying query 
- The window is defined by OVER clause


```
SELECT a.id, COUNT(a.id) OVER(PARTITION BY a.journal) FROM articles as a
```
