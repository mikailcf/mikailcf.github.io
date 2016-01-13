---
layout: inner
title: "Castaway"
type: castaway
---

### Intro

This project was made during the Programming Laboratory I course. It's the first course to give students what a project is like. Before that (and mostly after too) students only have to solve programming exercises (which are not by any means easy, but are a lot more focused on the topic being studied).

### Description

The objective of this simple game is to collect survivors from a shipwreck and take them to a rescue ship. You get points for collecting a survivor and more points for taking he/she to the rescue ship.

When hitting corals each player has a chance of dying, losing a life, respawning at a random location and losing the collected survivors.

### Development

The project was made in C with the Allegro library for graphics and input management. One of the learning goals for this project was how to deal with a program that has a main loop and states (something that's pretty much how you program most real-time games).

The survivors' movements are defined by a random function (it was a requirement), that's why they look frenetic.

Sprite animations are managed throught the use of a spritesheet. Also there was no helper function for drawing text with custom fonts on the screen, so I actually have all letters and numbers in a spritesheet and I implemented a function for drawing strings from that on the screen.

The video below is a short demo from the project (turn annotations on):

<iframe width="640" height="424" src="https://www.youtube.com/embed/2n1F4Ydc41E" frameborder="0" allowfullscreen></iframe>
