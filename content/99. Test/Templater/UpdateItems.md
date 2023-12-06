```
// Update Key Items
<%*
const dv = app.plugins.plugins["dataview"].api;
const filename = "List of key items";
const query = `LIST WITHOUT ID
FROM "5. Key items" and -[[List of key items]]
SORT file.name ASC`;

const tFile = tp.file.find_tfile(filename);
const queryOutput = await dv.queryMarkdown(query);

// write query output to file
await app.vault.modify(tFile, queryOutput.value);
%>
```