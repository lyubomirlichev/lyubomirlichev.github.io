---
title: Track Access VR Driver Demo
date: 2019-08-05
categories: [Pennant]
tags: [Windows, VR, Oculus Rift, Simulation, Demo, Unity]
pin: false
---

VR Train Operator Training - Proof of Concept / Demo

Pennant Rail’s Driver Training has been an industry-standard package for driver route learning and training for decades and is recognised and used throughout the UK by all leading Train and Freight Operating Companies.
It all began with a simple VR Proof Of Concept that I produced.

[Details](https://www.pennantplc.com/driver-training-2/)

### What I worked on
I worked on putting together a VR train driver experience, which uses an external [Thrustmaster t.Flight Hotas controller](https://www.thrustmaster.com/en-gb/products/t-flight-hotas-x/) to allow the user to control a train in VR.

How it works:

- I imported and optimised a custom model of the Darby Train station and a few kilometers of it's nearby rail surroundings. The model was heavily unoptimised, and not suitable for VR initially. For example, there were thousands of 3D assets of trees, instead of billboard trees.
- I set up a Cinemachine path along the rail tracks, starting a few miles away from the Darby Train station location.
- I set up a VR controller, and positioned it in the train's control seat, aligned with the seat and the thrust controls. 
- I built a system which takes in the input from the Thrustmaster controller, and processes and relays that into the Cinemachine system that controls the train's movement. The more thrust the user applied, the faster the train moved.

The Demo was used to demonstrate Pennant's capabilities in training and simulation, and ultimately lead to the acquisition of Track Access by Pennant.
