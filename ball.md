---
layout: inner
title: "Runner (WIP)"
type: ball
---

### Intro

I've started developing this game with mainly two goals in mind:

- learn Swift
- learn how to implement procedural content generation

In the same way as with <a href="{{ site.baseurl }}light/">Platformer</a> I'm making the game as a mean to learn. Given that I develop it during my free time, and that it's scarce, it'll probably not going to end up getting released.

### Description

As it's in early development and I'm changing mechanics as I go, I won't go into too much detail.

The game is an infinite runner with [eventually] procedural levels.

### Development

I'm using Apple's SpriteKit so I don't have to worry about graphics and physics and I can focus on the procedural algorithms.

I'm only using SpriteKit so I don't have to write the OpenGL for everything, but I'm managing the drawing myself, such as when to stop drawing elements that are not going to be visible anymore and free their memory, making the camera follow the character and whatnot.

What's done so far:

- simple level generation
- sprite-based tiles as well as player's simple animation
- smooth camera following for the character

Here's a video demonstrating the current features:

<iframe width="500" height="300" src="https://www.youtube.com/embed/B4Klspk-7jc" frameborder="0" allowfullscreen></iframe>
