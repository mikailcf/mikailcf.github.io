---
layout: inner
title: "Codename Ball (WIP)"
type: ball
---

### Intro Simple

I've started developing this game with mainly two goals in mind:

- learn Swift
- learn how to implement procedural content generation

In the same way as with <a href="{{ site.baseurl }}light/">Codename Light</a> I'm making the game as a mean to learn. Given that I develop it during my free time, and that it's scarce, it'll probably not going to end up getting released.

### Description

As it's in early development and I'm changing mechanics as I go, I won't go into too much detail.

The game is an infinite runner with procedural levels.

Basically what you'll be able to do is jump and I intend to implement some kind of attack too. I also intend to make the level have segments. The ideia is that each segment is going to have its own characteristics such as obstacle and enemy types. Players will know they entered a new segment through a change in the color palette throughout the level (also each segment is going to have their own set of features, but I haven't decided nor implemented that yet).

The objective is not to die. As an infinite runner the player should avoid obstacles and enemies (none of which are implemented yet in any way).

### Development

I'm using Apple's SpriteKit so I don't have to worry about graphics and physics and I can focus on the procedural algorithms.

I'm only using SpriteKit so I don't have to write the OpenGL for everything, but I'm managing the drawing myself, such as when to stop drawing elements that are not going to be visible anymore and free their memory, making the camera follow the character and whatnot.

What I've implemented so far is:

- level parallax
- procedural background drawing based on simple functions for generating points
- very simple procedural generation of the level ground
- character sprite trail for giving the notion of speed (I'll try to incorporate this trail in some mechanic too)
- world tinting to use when segment characteristics are decided
- smooth camera following for the character

What I intend to do next (in the short run) is:

- implement some kind of attack (I'll try to do something with the trail here)
- elaborate more on the ground generation so I have holes and maybe floating platforms too
- decide all the types of obstacles I'm going to have, and how they're going to be used in each segment

Here's a video demonstrating the current features:

<iframe width="640" height="361" src="https://www.youtube.com/embed/B4Klspk-7jc" frameborder="0" allowfullscreen></iframe>
