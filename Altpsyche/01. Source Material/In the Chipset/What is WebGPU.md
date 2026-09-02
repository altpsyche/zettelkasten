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

## Rough Notes

- In 1992, a company called Silicon Graphics created and released OpenGL, or Open Graphics Library.
- With this graphics API released, the next 10 years saw the rise of two major gaming companies: Sony with its flagship consoles PS1 and PS2, and Nintendo with the N64 and GameCube.
- Microsoft decided to get in on the action with its own graphics API called DirectX and launched Xbox in 2001
- For the next 10 years, even with the release of the Nintendo Wii, PS3, and Xbox 360. From 1990 to 2010, OpenGL and DirectX remained the most popular graphics APIs for console game developers.
- While the gaming industry was growing, so was the worldwide web.
- Khronos Group, who now worked on OpenGL, released WebGL—aka Web Graphics Library—in 2011
- WebGL is a JavaScript API that allows you to talk to the computer's GPU directly from the browser.
- While creating WebGL, the Khronos Group realized that OpenGL's architecture was suboptimal for modern graphics hardware and began working on Vulkan
- Around the same time, Apple also started working on its own modern graphics API for macOS and iOS called Metal.
- Now we had five different graphics APIs: WebGL, which was based on OpenGL, Metal, DirectX, and Vulkan.
- graphics space was becoming very fragmented.
- Google, Apple, Microsoft, Mozilla, the Khronos Group, Intel, and a bunch of other tech companies formed a group and started working on a new graphics API called WebGPU.
- At a high level, WebGPU is a graphics API that sits on top of DirectX, Vulkan, and Metal.
- WebGPU is a little confusing because you can use WebGPU outside of a web browser context.
- There's a WebGPU implementation for C++ called Dawn, and there's also a WebGPU implementation for Rust called wgpu.
- Fun fact: Bevy, the game engine written in Rust, uses wgpu under the hood.
- WebGPU aims to strike a good balance between performance and ease of use. It's faster than frameworks like OpenGL and WebGL and it's easier to set up and use than frameworks like Metal, Vulkan, and DirectX.
- For reference, it takes 800 to 1,000 lines of code to draw a simple triangle in Vulkan. It can take more than 400 lines of code in DirectX 12. And in comparison, it takes 70 lines of code to draw a triangle in WebGL and about 100 lines of code in WebGPU.
- Think of WebGPU as being the successor to WebGL
- WebGPU allows you to do two basic things: draw triangles, points, and lines to textures and run computations on the GPU.
- Drawing triangles, is something we could already do in WebGL. But running computations on the GPU is what WebGPU does which WebGL doesnt.
- WebGPU API doesn't require you to work with global state, which was considered a downside of WebGL.
- WebGPU API is also a little faster because it's a wrapper around the more modern APIs: Vulkan, DirectX, and Metal

## Background

| When         | What happened                                           | Why it matters                                                           |
| ------------ | ------------------------------------------------------- | ------------------------------------------------------------------------ |
| 1992         | Silicon Graphics releases OpenGL                        | one portable graphics API, works everywhere                              |
| 1990s        | Sony ships PS1 and PS2, Nintendo ships N64 and GameCube | console generation built on that API                                     |
| 2001         | Microsoft ships DirectX and Xbox                        | second API, Windows and Xbox only                                        |
| 1990 to 2010 | OpenGL and DirectX run console development              | Wii, PS3 and Xbox 360 era. two APIs, stable landscape                    |
| 2011         | Khronos releases WebGL                                  | JavaScript reaches the GPU from the browser. built on OpenGL             |
| 2014         | Apple starts Metal (mine)                               | macOS and iOS only                                                       |
| 2016         | Vulkan 1.0 (mine)                                       | Khronos found OpenGL a poor fit for modern hardware while building WebGL |
| 2017 onward  | consortium forms around WebGPU (mine)                   | Google, Apple, Microsoft, Mozilla, Khronos, Intel                        |

Rows marked *(mine)* are dates added from outside the video. Verify before publishing any of them.

The shape of it: one portable API, then a decade of two, then a split into three platform specific modern APIs. WebGPU is the attempt to put one portable layer back on top.

## Claims
- WebGPU exists because the graphics API landscape fragmented. Vulkan, Metal and DirectX 12 each replaced an older API on one platform, which left no portable modern option.
- WebGPU is a layer over Vulkan, Metal and DirectX rather than a new low level API of its own.
- WebGPU is not browser only. Dawn implements it for C++, wgpu for Rust, and Bevy runs on wgpu.
- WebGPU aims at the middle of the performance and difficulty trade-off. Faster than WebGL, easier than Vulkan.
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
