---
layout: inner
title: "Simple AR Game"
type: ar_game
---

### Intro

This game project was made during college, in the course following the <a href="{{ site.baseurl }}castaway/">Castaway</a> course, back in 2010.
The idea was that everyone had to make an AR-based project, games allowed.

### Description

Each cube face has its own marker and represents a different set of obstacles within the cube (represents a different _room_).

Players can use gravity to move the ball around one room by rotating the cube, and thus, the room. The objective is to get the ball to the finishing point and to achieve this players must switch the currently tracked cube face (switch rooms).

The ball's movement is fixed in two dimensions within a room and when switching from one room to another the ball stays in the same position as previously. With that the player is able to complete each level.

### Development

The game was made in ActionScript 3 (Flash) with three libraries, one for physics (JigLib), one for 3D graphics (Papervision3D) and another for augmented reality (FLARManager).

In the video below I show the first time I've managed to achieve the "hole" effect in AR. This might look easy for someone with some computer graphics knowledge, but I had none at the time. This was my first attempt at 3D graphics programming.

<iframe width="500" height="300" src="http://www.youtube.com/embed/_bcb7aV6zTg" frameborder="0" allowfullscreen></iframe><br><br>

That was achieved by making a filter matrix that applied an "invisible" mask to the green color. So that's actually a whole cube with green outside faces.

Below is a video with simple shading and menus.

<br><br><iframe width="500" height="300" src="http://www.youtube.com/embed/st9zMsYVs_E" frameborder="0" allowfullscreen></iframe><br><br>

And this is what the "final" version of the project looks like:

<br><br><iframe width="500" height="300" src="http://www.youtube.com/embed/T6PMxGAjBeE" frameborder="0" allowfullscreen></iframe>

<iframe width="500" height="300" src="http://www.youtube.com/embed/sMptS2Nfar0" frameborder="0" allowfullscreen></iframe>
