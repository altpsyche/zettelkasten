---
type: literature
medium: video
created: 2026-09-01
source: YouTube
author: Suboptimal Engineer
channel: Suboptimal Engineer
url: https://www.youtube.com/watch?v=oIur9NATg-I
status: read
tags:
  - source
  - webgpu
---

# What is WebGPU?

**Source:** YouTube
**Author:** Suboptimal Engineer
**Link:** https://www.youtube.com/watch?v=oIur9NATg-I

## Background

| When | What happened | Why it matters |
|---|---|---|
| 1992 | Silicon Graphics releases OpenGL | one portable graphics API, works everywhere |
| 1990s | Sony ships PS1 and PS2, Nintendo ships N64 and GameCube | console generation built on that API |
| 2001 | Microsoft ships DirectX and Xbox | second API, Windows and Xbox only |
| 1990 to 2010 | OpenGL and DirectX run console development | Wii, PS3 and Xbox 360 era. two APIs, stable landscape |
| 2011 | Khronos releases WebGL | JavaScript reaches the GPU from the browser. built on OpenGL |
| 2014 | Apple starts Metal (mine) | macOS and iOS only |
| 2016 | Vulkan 1.0 (mine) | Khronos found OpenGL a poor fit for modern hardware while building WebGL |
| 2017 onward | consortium forms around WebGPU (mine) | Google, Apple, Microsoft, Mozilla, Khronos, Intel |

Rows marked *(mine)* are dates added from outside the video. Verify before publishing any of them.

The shape of it: one portable API, then a decade of two, then a split into three platform specific modern APIs. WebGPU is the attempt to put one portable layer back on top.

## Claims
- WebGPU exists because the graphics API landscape fragmented. Vulkan, Metal and DirectX 12 each replaced an older API on one platform, which left no portable modern option.
- WebGPU is a layer over Vulkan, Metal and DirectX rather than a new low level API of its own.
- WebGPU is not browser only. Dawn implements it for C++, wgpu for Rust, and Bevy runs on wgpu.
- WebGPU aims at the middle of the performance and difficulty tradeoff. Faster than WebGL, easier than Vulkan.
- His evidence for that is lines of code to draw a triangle: Vulkan 800 to 1000, DirectX 12 over 400, WebGPU around 100, WebGL 70. His figures, unverified.
- WebGPU does two things: draw primitives to textures, and run compute on the GPU. Compute is what WebGL cannot do.
- WebGPU drops the global state model. He treats WebGL global state as its main design flaw.
- He frames WebGPU as the successor to WebGL rather than a parallel option.

## Quotes and timestamps
- [00:00] 

## My reading


## Teaching observations
- He spends the first stretch on 20 years of history before saying what WebGPU is. Decide whether your chapter 1 earns that, or whether the reader wants running code first.
- 

## Extracted
- [[]]

## Project
- [[Series Outline]]
