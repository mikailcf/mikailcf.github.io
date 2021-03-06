---
layout: inner
title: "Runner (WIP)"
type: runner
---

### Intro

This is a personal project. I've started developing this game with mainly two goals in mind:

- learn Swift
- learn how to implement procedural content generation

### Description

As it's in early development and I'm changing mechanics as I go, I won't go into too much detail.

The game is an infinite runner with [eventually] procedural levels.

### Development

I'm using Apple's SpriteKit so I don't have to worry about graphics and physics and I can focus on the procedural algorithms.

I'm only using SpriteKit so I don't have to write the OpenGL for everything, but I'm managing the drawing myself, such as when to stop drawing elements that are not going to be visible anymore and free their memory, making the camera follow the character and whatnot.

What's done so far:

- simple level generation
- sprite-based tiles
- simple sprite animation
- smooth camera following for the character

Here's a video demonstrating the current features:

<iframe width="500" height="300" src="https://www.youtube.com/embed/VIjTjPErQ3k" frameborder="0" allowfullscreen></iframe>
