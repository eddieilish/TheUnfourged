```
// Update Factions
<%*
const dv = app.plugins.plugins["dataview"].api;
const filename = "List of factions";
const query = `LIST WITHOUT ID
FROM "4. Factions" and -[[List of factions]]
SORT file.name ASC`;

const tFile = tp.file.find_tfile(filename);
const queryOutput = await dv.queryMarkdown(query);

// write query output to file
await app.vault.modify(tFile, queryOutput.value);
%>
```