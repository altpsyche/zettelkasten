---
type: project
created: 2026-09-01
status: planning
tags:
  - project
  - wgsl
---

# Shader Fundamentals with WGSL

The spine. What the series is, who it is for, and what order it teaches in.

## Premise

*One sentence. Why this exists when other WGSL material already does.*


## Who this is for

*"Beginners" is not an audience. Someone who writes JS but has never written a shader, and someone coming from GLSL, want different series.*


## What the reader can do at the end


## What I assume they already know

*The assumption you get wrong here is the one that loses readers in chapter 2.*


## Scope

**In:**

**Out:**

*Naming what you refuse to cover is what keeps a series finishable.*

## Chapters

```dataview
TABLE WITHOUT ID chapter AS "#", file.link AS Title, idea AS "The one new idea", status AS Status
FROM "06. Projects/Shader Fundamentals with WGSL/Chapters"
SORT chapter ASC
```

New chapter: command palette, *Templater: Create new note from template*, pick Chapter Draft.

## Order decisions

*The reasoning outlives the list.*
- WebGPU first because WGSL cannot run without a host. Revisit if that turns out to front-load too much setup.

## Sources

```dataview
TABLE WITHOUT ID file.link AS Source, author AS Author, medium AS Medium, status AS Status
FROM "01. Source Material"
WHERE contains(file.outlinks, this.file.link)
SORT status ASC
```

## Open questions
- 
