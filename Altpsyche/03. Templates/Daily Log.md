---
type: log
date: <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
tags:
  - log
---

# <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>

## Log
<% tp.file.cursor(1) %>

## Captured today
```dataview
LIST FROM "00. Fleeting Notes" WHERE file.cday = date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>)
```

## Processed
```dataview
LIST FROM "04. Zettelkasten" WHERE file.cday = date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>)
```
