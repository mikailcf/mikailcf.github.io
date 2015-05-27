---
layout: post
title: 
super: ar_game
---

### Intro

This game project was made during the Programming Laboratory II course (the -link to castaway here- was made during Programming Laboratory I) back in 2010. It's the second course with the objective of showing the students what a bigger project looks like since most other courses are based on smaller, but by no means easier, programming exercises that focus on algorithms or problem solving.

The professor teaching the course at the time was specialized in computer vision and was very intered in augmented reality. With that he stabilished that all projects should ba based on AR and that people were free to make game projects if they wanted.

<!-- I was in a group with two other friends but I ended up doing pretty much the whole thing by myself. What was ultimately a good thing for me given that I got to learn a lot more (with the downside of sleeping a lot less). -->

<!-- My group brainstormed and settled with my conecpt of a cube based game where basically the player had to use the gravity to move a ball through obstacles to get to the goal point and that each face of the cube should have its own set of obstacles. We came up with ideas like: multiple cubes to where the ball could go to if they were side by side, the player being able to move obstacles between cube faces. But sadly given that there were more courses and tests during the semester and that I've found out that I couldn't count with the others the final implementation ended up with being just the basic concept. -->

### Description

Each cube face has its own marker and represents a different set of obstacles within the cube (represents a different _room_).

Players can use gravity to move the ball around one room by rotating the cube, and thus, the room. The objective is to get the ball to the finishing point and to achieve this players must switch which cube face is currently being tracked (switch rooms).

The ball's movement is fixed in two dimensions within a room and when switching from one room to another the ball stays in the same position. With that the player is able to complete each level.

### Development

It was made in ActionScript 3 (Flash) with three libraries, one for physics (JigLib), one for 3D graphics (Papervision3D) and another for augmented reality (FLARManager).

In the video below I show the first time I've managed to achieve a "hole" effect in AR. This might look easy for someone with some computer graphics knowledge, but I had none at the time. This was my first attempt at 3D graphics programming.

<iframe width="640" height="380" src="http://www.youtube.com/embed/_bcb7aV6zTg" frameborder="0" allowfullscreen></iframe>

That was achieved by making a filter matrix that applied an "invisible" mask to the color green. So that's actually a whole cube with green outside faces.

<iframe width="640" height="380" src="http://www.youtube.com/embed/l2Y8p3s_5k8" frameborder="0" allowfullscreen></iframe>
<iframe width="640" height="380" src="http://www.youtube.com/embed/st9zMsYVs_E" frameborder="0" allowfullscreen></iframe>

### "Final" version
<iframe width="640" height="380" src="http://www.youtube.com/embed/T6PMxGAjBeE" frameborder="0" allowfullscreen></iframe>
<iframe width="640" height="380" src="http://www.youtube.com/embed/sMptS2Nfar0" frameborder="0" allowfullscreen></iframe>
<iframe width="640" height="380" src="http://www.youtube.com/embed/TPY2e6tHm_g" frameborder="0" allowfullscreen></iframe>

<!-- https://www.youtube.com/watch?v=_bcb7aV6zTg     hole

https://www.youtube.com/watch?v=l2Y8p3s_5k8     physics

https://www.youtube.com/watch?v=st9zMsYVs_E     shading and menu

https://www.youtube.com/watch?v=T6PMxGAjBeE     qub 1 2
https://www.youtube.com/watch?v=sMptS2Nfar0     qub 3 4
https://www.youtube.com/watch?v=TPY2e6tHm_g     qub 5 -->