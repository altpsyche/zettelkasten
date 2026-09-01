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

Also out, and worth saying because the title implies otherwise: the vertex stage, and textures or image sampling. Everything here is procedural, drawn in a fragment or compute shader.

## Chapter arc

Planned order. Each line is one chapter. Numbers move as chapters get written.

No maths chapter. Each chapter introduces only the maths its own technique needs, so an artwork is never more than one chapter away.

**Foundations**
1. WGSL on WebGPU. Includes what GLSL readers need to remap.
2. The pixel and its coordinates
3. Shaping functions. Ends by plotting `length(uv)` as a radial gradient, without naming it.

**Distance fields**
4. Signed distance: the field, one shape, a clean edge. Names the gradient from chapter 3
5. Combining: union, subtraction, smooth minimum
6. Bending space: transform, repeat, warp

**Colour**
7. Colour, mixing, cosine palettes, and why a ramp lies

**Noise**
8. Randomness, noise functions, hashing
9. Voronoi and cellular noise
10. Fields: octaves and fractional Brownian motion

**Motion**
11. Motion: flow, looping, domain warping

**Compute**
12. Compute shaders: workgroups, storage buffers, ping-pong between frames
13. Multi-scale Turing patterns. Reaction diffusion, run as compute

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
- Anti-aliasing is taught at the first edge, in chapter 4, rather than as its own chapter. It is a technique attached to drawing an edge, not a separate idea.
- Chapter 3 ends on a radial gradient that is a distance field in all but name. Chapter 4 names it. The jump from one dimensional curves to reading a two dimensional field is the steepest seam in the first half, and this makes the new idea a label for something the reader already built.
- Debugging lives in [[Debugging Shaders]] rather than in a chapter. Failure modes get written down while writing each chapter, and the page ships as an appendix.
- 3D raymarching ships as series two. Chapters 1 to 10 are one coherent thing: patterns on a plane. Raymarching changes the mental model and deserves its own run.

## Sources

```dataview
TABLE WITHOUT ID file.link AS Source, author AS Author, medium AS Medium, status AS Status
FROM "01. Source Material"
WHERE contains(file.outlinks, this.file.link)
SORT status ASC
```

## Open questions

- Does the playground support storage buffers and compute passes today? Chapters 12 and 13 depend on it. Blocking.
- Where do the GLSL comparisons live? Chapter 1 section, inline asides in every chapter, or an appendix. Inline serves them best and taxes the artists in every chapter.
- Chapter 11 to 12 is the real cliff in this series. New mental model, new pipeline stage, new failure modes. Does 12 need to split into language and pipeline?
- Turing patterns as compute is the plan. Worth checking it still works as a fragment shader, since that would drop 12 as a hard prerequisite for 13.
- 13 chapters again, after trimming to 10. Still one run, or does Foundations through Colour ship first?
