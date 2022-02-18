# Filter query using NOT EXISTS

Find all parents who live on 5th avenue and whose children are not adult or have no children 

```
SELECT
	distinct count(t1.id)
FROM
	"Parent" t1
WHERE
	t1.street = '5th avenue'
	AND NOT EXISTS (
		SELECT
			1
		FROM
			"Parent" AS t2
			JOIN "Child" t3 ON t3.parent_id = t2.id
				AND t3.adult = 't'
		WHERE t2.id = t1.id)
```
