```dataview
TABLE
	rows.file.link AS "Name",
	rows.type AS "Type"
FROM "3. Places"
GROUP BY category AS Group
SORT columnB ASC, columnC ASC
```