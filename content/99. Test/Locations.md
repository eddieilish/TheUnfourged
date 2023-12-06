---
draft: true
---
```dataview
TABLE
join(rows.file.link, "<br>") AS Name,
join(rows.type, "<br>") as Type
FROM "3. Locations"
GROUP BY category AS Category
SORT columnA ASC, columnB ASC, column
```

