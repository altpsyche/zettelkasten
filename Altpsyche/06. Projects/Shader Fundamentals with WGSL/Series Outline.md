---
type: project
created: 2026-09-01
status: planning
tags:
  - project
  - wgsl
---

# Shader Fundamentals with WGSL

## Premise

Teach modern shading techniques as a way to make art. One concept per chapter, and every chapter ends with a finished artwork built from that concept in WGSL.

Published on altpsyche.dev, which runs a live WGSL playground. Readers edit and run every example in the page. No local setup, no renderer to build.

## Who this is for

Two readers, and every chapter has to serve both.

**Artists from node graphs.** Work in CG, understand shading conceptually through material graphs, have never written shader code by hand. They come for the artwork and stay if the maths arrives in small pieces.

**Developers coming from GLSL.** Already write shaders. They come for WGSL specifically, and for compute, which GLSL never gave them on the web.

Not for absolute programming beginners.

## What the reader can do at the end

Read and write WGSL fragment shaders without a reference open, and write a compute pass that carries state between frames. Look at an effect and recognise which technique produces it. Combine pattern, colour and motion deliberately rather than by trial.

## What I assume they already know

- What a shader is, and roughly where it sits in a pipeline
- Material work in a node graph, so terms like normal, UV and mix are familiar
- Reading and writing code: functions, loops, types
- A broad sense of graphics APIs, without any WebGPU experience

GLSL readers can skip the shading concept explanations and read the WGSL and compute material directly.

## Scope

**In:** everything in the chapter arc below, plus GPU compute: workgroups, storage buffers, and simulation that runs between frames.

**Out:** how to write a renderer, programming basics, making games, WebGPU in depth. The playground is the host, so none of that is needed to follow along.

## Chapter arc

Planned order. Each line is one chapter. Numbers move as chapters get written.

No maths chapter. Each chapter introduces only the maths its own technique needs, so an artwork is never more than one chapter away.

**Foundations**
1. WGSL on WebGPU. Includes what GLSL readers need to remap.
2. Shaping functions

**Distance fields**
3. Signed distance: union, subtraction, smooth minimum
4. Bending space

**Colour**
5. Colour, mixing, cosine palettes, and why a ramp lies

**Noise**
6. Randomness, noise functions, hashing
7. Fields: octaves and fractional Brownian motion

**Motion**
8. Motion: flow, looping, domain warping

**Compute**
9. Compute shaders: workgroups, storage buffers, ping-pong between frames
10. Multi-scale Turing patterns. Reaction diffusion, run as compute

### Series two, later

Raymarching is a different mental model and ships separately.

1. Raymarch: distance in 3D and the march loop. Budget: step count
2. Light: the gradient as a normal, and one lamp
3. Scattering, absorption, and the finished frame. Budget: march and scattering samples

## Chapters written

```dataview
TABLE WITHOUT ID chapter AS "#", file.link AS Title, idea AS "The one new idea", status AS Status
FROM "06. Projects/Shader Fundamentals with WGSL/Chapters"
SORT chapter ASC
```

New chapter: command palette, *Templater: Create new note from template*, pick Chapter Draft.

## Order decisions

- WebGPU gets an introduction only, no renderer setup. The altpsyche.dev playground is the host, so readers write shader code from chapter 1 with nothing to install. Cost: the playground has to keep working, and it is now a dependency of the series.
- No maths chapter. Maths arrives per chapter, at the moment its technique needs it. Front-loading maths is where art-driven series lose the artists.
- Compute is in, because GLSL readers came for the thing GLSL never gave them on the web. It sits at 9 and 10, after motion, because Turing patterns need it and make a payoff worth the setup.
- 3D raymarching ships as series two. Chapters 1 to 10 are one coherent thing: patterns on a plane. Raymarching changes the mental model and deserves its own run.

## Sources

```dataview
TABLE WITHOUT ID file.link AS Source, author AS Author, medium AS Medium, status AS Status
FROM "01. Source Material"
WHERE contains(file.outlinks, this.file.link)
SORT status ASC
```

## Open questions

- Where do the GLSL comparisons live? Chapter 1 section, inline asides in every chapter, or an appendix. Inline serves them best and taxes the artists in every chapter.
- Is one compute chapter enough before Turing patterns, or does 9 split into language and pipeline?
- Turing patterns as compute is the plan. Worth checking it still works as a fragment shader, since that would remove chapter 9 as a hard prerequisite.
- Does the playground support storage buffers and compute passes today? Chapters 9 and 10 depend on it.
