---
draft: true
---
```
// Update Publish Files.md
<%*
const dv = app.plugins.plugins["dataview"].api;
const filename = "List of characters";
const query = `LIST WITHOUT ID
FROM "2. Characters" and -[[List of characters]]
SORT file.name ASC`;

const tFile = tp.file.find_tfile(filename);
const queryOutput = await dv.queryMarkdown(query);

// write query output to file
await app.vault.modify(tFile, queryOutput.value);
%>
```