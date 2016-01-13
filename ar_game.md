---
layout: inner
title: "Simple AR Game"
type: ar_game
---

### Intro

This game project was made during the Programming Laboratory II course (the <a href="{{ site.baseurl }}castaway/">Castaway</a> was made during Programming Laboratory I) back in 2010. It's the second course with the objective of showing the students what a bigger project looks like since most other courses are based on smaller, but by no means easier, programming exercises that focus on algorithms or problem solving.

The professor teaching the course at the time was specialized in computer vision and was very intered in augmented reality. With that he stabilished that all projects should ba based on AR and that people were free to make game projects if they wanted.

### Description

Each cube face has its own marker and represents a different set of obstacles within the cube (represents a different _room_).

Players can use gravity to move the ball around one room by rotating the cube, and thus, the room. The objective is to get the ball to the finishing point and to achieve this players must switch which cube face is currently being tracked (switch rooms).

The ball's movement is fixed in two dimensions within a room and when switching from one room to another the ball stays in the same position. With that the player is able to complete each level.

### Development

It was made in ActionScript 3 (Flash) with three libraries, one for physics (JigLib), one for 3D graphics (Papervision3D) and another for augmented reality (FLARManager).

In the video below I show the first time I've managed to achieve the "hole" effect in AR. This might look easy for someone with some computer graphics knowledge, but I had none at the time. This was my first attempt at 3D graphics programming.

<iframe width="640" height="380" src="http://www.youtube.com/embed/_bcb7aV6zTg" frameborder="0" allowfullscreen></iframe>

That was achieved by making a filter matrix that applied an "invisible" mask to the green color. So that's actually a whole cube with green outside faces.

Below is a video with simple shading and menus.

<iframe width="640" height="380" src="http://www.youtube.com/embed/st9zMsYVs_E" frameborder="0" allowfullscreen></iframe>

## "Final" version

In the next videos I show the final version of the game.

<iframe width="640" height="380" src="http://www.youtube.com/embed/T6PMxGAjBeE" frameborder="0" allowfullscreen></iframe>

<iframe width="640" height="380" src="http://www.youtube.com/embed/sMptS2Nfar0" frameborder="0" allowfullscreen></iframe>

To easily create levels the game simply reads descriptive matrices and build them on the fly. Some examples are:

```
```

The game is not bound to a specific matrix size, it reads the matrix and extracts the size from it. That way I can build simple levels with far less information than needed for more complex ones.
