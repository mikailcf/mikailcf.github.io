---
layout: inner
title: "Platformer (WIP)"
type: platformer
---

### Intro

This is a personal project. My objectives developing this are to:

- implement mechanics such as physics and lightning
- learn some image processing techniques such as blur implementation
- learn shaders

### Description

This is a 2D platformer where the player must use some lightning mechanics to traverse the world and solve puzzles.

It's on very early development stages so only the basic physics and lightning parts are implemented. No mechanics are implemented yet.

### Development

I'm using C++ for this one, with the SFML library for graphics and input management. The physics and lightning are implemented by me, no extra libraries.

Some features are:

- shadows during the level
- soft shadows with blur in the menu
- blocks that become invisible in the shadow (_hidden blocks_)
- block animations

The levels are built based on a text file following a very simple descriptive syntax.
The level for the video below is described as:

```
# a block is defined by
#  x y width height R G B is_hidden is_animated
#
# definition of an animation is basically the total time, accelerating 
# and breaking times and the vector that defines each animation segment

4 1  # number_of_blocks number_of_hidden_blocks
1027 609 291 38 120 120 120 0 1
3  # animation segments 
3.5 1 0 57 -229 0.2 0.2
3.5 1 0 312 125 0.2 0.2 
3.5 1 0 -369 104 0.2 0.2 
1 
616 486 366 38 120 120 120 1 0 
247 556 392 38 120 120 120 0 0 
0 609 269 38 120 120 120 0 0 
64 336 
```

For me not to have to build a level editor I've written a simple script for Photoshop to take care of that. It reads basic layer information, like position and size, and writes an output in the exact same format the game reads. It does that based on the layer name (the name defines if it's a hidden block, animated block or normal block).

For the soft shadows in the menu I've implemented a simple radial blur based on distance from the light source. For the shadows during the level I'm using a combination of polygon drawing, shader for the radial light and rendering based on the stencil buffer.

Here's a video demonstration:

<iframe width="500" height="300" src="https://www.youtube.com/embed/K80JfZgXPwM" frameborder="0" allowfullscreen iv_load_policy="1"></iframe>

