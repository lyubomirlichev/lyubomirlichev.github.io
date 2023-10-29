---
title: Parachute mini game
date: 2018-05-18
categories: [Pennant]
tags: [Windows, VR, Oculus Rift, Gameplay, Unity]
pin: false
---

### Project description
The Parachute mini game is a simplified version of the VPTS system, with added engaging game mechanics. The player starts off having already deployed their parachute. The player then is tasked to use the toggles to navigate through as many rings as possible, on their way down to the landing zone.

The game was used on shows events, as an entry point, to let visitors try out the parachute simulation within a simple and engaging context.

Demo:

{% include embed/youtube.html id='yQ4s77aJ2zQ' %}

### What I worked on
Adapted parachute control system from VPTS, terrain loading, and input system. Added game rings for the player to aim to go through, and a score tracking system. Whenever the player goes through a ring, the next one lights up. Whenever the player crosses a ring, the system tells them how close they were to the center through a positive UI message. Also implemented a decal shader to mark the landing zone, to simulate a spray-paint target. 
