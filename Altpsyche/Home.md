---
type: index
tags:
  - home
---

# Altpsyche

Entry point. Bookmark this.

## The vault

| Folder | Holds | Lifespan |
|---|---|---|
| `00. Fleeting Notes` | raw capture, unprocessed | days: process or delete |
| `01. Source Material` | literature notes, one per source | permanent, but not *thinking* |
| `02. Indexes` | MOCs: hand-built entry points into the slip-box | grows slowly |
| `03. Templates` | note scaffolds | rarely touched |
| `04. Zettelkasten` | **the slip-box.** permanent notes, flat, ID-named | forever |
| `05. Thought Logs` | daily notes | append-only |
| `06. Projects` | drafts and scratch, one folder per project | dies when the project ships |

`In the Chipset` = digital origin. `In the Flesh` = physical origin. Applies to `00` and `01` only.

## How this works

See [[Workflow]]. Short version: capture → process → link. Never skip link.

## Active projects

- [[Series Outline|Shader Fundamentals with WGSL]]. Chapter 1 drafting.

## Indexes

<!-- add a line here for every MOC you create in 02. Indexes -->
- 

## Reading

```dataview
TABLE WITHOUT ID file.link AS Source, author AS Author, status AS Status
FROM "01. Source Material"
WHERE type = "literature"
SORT status ASC
```

## Health check

Notes that broke rule 3. Fix or delete.

```dataview
TABLE WITHOUT ID file.link AS Note, length(file.outlinks) AS Links
FROM "04. Zettelkasten"
WHERE length(file.outlinks) < 2
```

Fleeting notes past their week. Promote or bin.

```dataview
TABLE WITHOUT ID file.link AS Note, file.cday AS Captured
FROM "00. Fleeting Notes"
WHERE file.cday <= date(today) - dur(7 days)
SORT file.cday ASC
```
