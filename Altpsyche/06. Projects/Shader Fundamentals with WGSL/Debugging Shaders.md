---
type: project
created: 2026-09-02
status: growing
tags:
  - project
  - wgsl
---

# Debugging Shaders

Part of [[Series Outline]]. Ships as an appendix, not a chapter.

Shaders have no breakpoints and no print. The whole skill is turning an invisible number into something you can look at. Readers hit this in chapter 3, well before they have vocabulary for it.

Fill this in while writing chapters, not afterwards. Every failure you hit while building an example is one a reader will hit, and you stop being able to see it once the code works.

## Seeing a value

The core move: assign the value to colour and look at it. Collect the idioms that work.

## Symptom to cause

| What you see | Usually means |
|---|---|
| black screen |  |
| white screen |  |
| jagged edges |  |
| banding |  |
| flickering |  |
| nothing after an edit |  |

## Fragment stage

## Compute stage

Different failure modes from fragment work, and the reason chapter 11 to 12 is the steepest jump in the series. Workgroup sizing, buffer synchronisation, reading a buffer while it is being written, ordering between passes.

## WGSL specific

Things that compile in GLSL and do not here, or fail differently.

## Playground specific

altpsyche.dev quirks worth telling readers about.
