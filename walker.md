---
layout: inner
title: "Walker"
type: walker
---

### Intro

Another college project, for the Computer Graphics course. The idea was to make a simple 3D walking game using only OpenGL. As the new API introduced with OpenGL 3.0 was still relatively new then and our professor wasn't familiar with it we went with the older 2.x API.

### Description

In this project we had to simulate walking on the outside of the buildings from our institute while implementing some techniques such as:

- changing the projection matrix for shadow rendering and orthographic rendering of text
- only rendering particles within an area around the camera
- skybox

Some must-have features were:

- shadows
- rain with 3D raindrops
- a skybox
- display the frame rate

Some optional features (that I implemented) were:

- day and night cycle
- fog during the rain
- lightning bolts during the rain
- trees
- collision check

### Development

The project was made wich C++ and OpengGL. No third party libraries.

We could use libraries for loading JPEGs and 3D models and such if we wanted but I decided to do everything myself just so I could have an idea how difficult it was to implement this kind of functionality. Of course I went with a simplified version for each of these elements (I loaded RAWs and not JPEGs and I made my own 3D model format) but I think I learned what I wanted going this way.

To illustrate the model format, here's the model for the Block B Building (blue building in the video below):

```
# each line represents a polygon (wall) and follows the format:
#  width height x y z facing_direction texture

32  # number of vertices
30  28 -23  -190 14 s assets/tex/01.raw
190 28 -8   -95  14 e assets/tex/02.raw
30  28 -23  0    14 n assets/tex/04.raw
126 28 -38  63   14 e assets/tex/03.raw
30  28 -53  126  14 n assets/tex/01.raw
30  28 -68  111  14 w assets/tex/04.raw
30  28 -83  96   14 n assets/tex/01.raw
30  28 -98  111  14 e assets/tex/04.raw
30  28 -113 126  14 n assets/tex/01.raw
90  28 -128 81   14 w assets/tex/05.raw
60  28 -128 6    14 w assets/tex/09.raw
30  28 -113 -24  14 s assets/tex/10.raw
30  28 -98  -39  14 w assets/tex/10.raw

112 17 -184 36   8.5 n assets/tex/06.raw
60  17 -240 6    8.5 w assets/tex/07.raw
30  17 -225 -24  8.5 s assets/tex/08.raw
30  17 -210 -39  8.5 w assets/tex/07.raw
112 17 -154 -54  8.5 s assets/tex/06.raw

136 28 -98  -122 14 w assets/tex/11.raw

20  14 -108 -130 6.7 n assets/tex/24.raw
66  17 -151 -100 8.5 n assets/tex/22.raw
90  17 -184 -145 8.5 w assets/tex/23.raw
66  17 -151 -190 8.5 s assets/tex/22.raw
90  17 -118 -145 8.5 e assets/tex/23.raw
20  14 -108 -160 6.7 s assets/tex/24.raw

30  28 -83  -190 14 s assets/tex/01.raw
60  28 -68  -160 14 e assets/tex/13.raw
30  28 -53  -130 14 s assets/tex/14.raw
60  28 -38  -160 14 w assets/tex/13.raw

30  17 -53 -190  8.5 s assets/tex/12.raw
```

The facing direction of each wall is also used for collision detection purposes. I basically check for intersections between the player's bounding box and the walls, and I set to zero the component in player's velocity that is going in the oposite direction of the facing direction of the wall.

The format for the textures is a RAW file with three bytes for each pixel (RGB) and the format for the masks (I implemented masking for any renderable texture) is a RAW file with one byte for each pixel (the alpha value).

For rendering the text for the fps count and the "lightning" I just use a orthographic matrix for projection and for the shadows rendering I need only to make a 3D transformation on the projection matrix to make it a perspective projection from the light source point of view and projected to the ground.

The raindrops are small cones and are reutilized after they hit the ground.

Below is a video demonstration (turn annotations on):

<iframe width="500" height="300" src="http://www.youtube.com/embed/8a1UOAVBPXk" frameborder="0" allowfullscreen></iframe>
