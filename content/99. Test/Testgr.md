---
draft: true
---
```dataview
table
file.name as name,
map(rows, (r) => (Region = r.region[0] and Category = r.category[0] and "Number of files" = length(r.rows)))
from "3. Locations"
group By Category
group By Region
```
