---
title: VR Parachute Simulator
date: 2019-05-22
categories: [Pennant]
tags: [Windows, VR, Simulation, Oculus Rift, HTC Vive, Unity]
pin: true
---


### Project description
The Parachute Trainer is an immersive training system capable of supporting initial canopy control training and malfunction recognition through to mission planning and rehearsal.

[Details](https://www.pennantplc.com/parachute-trainer/#)

Trailer:

[![Image alt text](https://img.youtube.com/vi/suy02gP9J1Y/0.jpg)](https://www.youtube.com/watch?v=suy02gP9J1Y)

[Overview Brochure](https://www.pennantplc.com/wp-content/uploads/2023/09/Parachute_Trainer_2023.pdf)

### What I worked on
#### After-Action Replay system
One of the offerings of the simulator is the capability to record scenarios for later viewing. Specifically, all of the parameters of the scenario are recorded every frame, and then the scenario is reloaded and driven by the saved data. I architected and implemented this feature from with guidance from my team. 

How it works:
 
1. The scenario is configured by the instructor. All students/players (up to 24) connect to a shared lobby.
2. The instructor starts the scenario when every player is ready. As this is a multiplayer application, the instructor acts as a host and receives all of the data of the other players.
3. The instructor's application records the scenario behind the scenes into a unique binary file. For every frame all non-deterministic transforms and saved, and all session states and transitions are saved, including animations. During this time, the instructor can also observe each student, create bookmarks, and trigger faults.
4. Once the session has ended, the instructor can navigate to the ARR mode, also available offline. 
5. ARR mode will allow the instructor to load an instance of the unique binary file, and effectively begin a new scenario with a controllable timeline. The system provides playback controls, multiple fixed camera positions for each player, and a free-roam camera. The instructor can use the system to asses each student's performance, reaction time, behaviour, and more.
6. The instructor can also observe and export all of the stats, scores, and performance of the students in a separate screen.

#### Logger system
I designed and implemented a logger system, which records all of the students' actions into a single modern UI, allowing the instructor to analyze them during and after a training session. The data can also be exported to .pdf for later viewing.

#### Deterministic flight path
The VPTS simulator provides accurate terrain simulations for multiple different types of terrains.

As part of the terrain configuration, I implemented:
- Allowing the instructor to configure the duration of flight before students jump out. Can be configured up to 2 hours, and is implemented in such a way that the observers from the plane will never see the edges of the terrain. 
- Allowing the instructor to configure the angle of approach relative to the terrain.
- Allowing the instructor to designate an exact time at which the plane will be over the DZ.
- Allowing the instructor to configure a desired flight altitude.

As the terrains can be up to 200kmx200km, modifying objects at that scale introduces floating point precision issues. Therefore, the system actually keeps the plane and player at the center of the world, and moves everything else relative to the plane. The system I designed effectively rotates and positions the entire terrain relative to the plane, so as to make it appear that the plane is flying in wide circles around the terrain. Similarly to winding back a clock, I was able to calculate exactly how many laps around the terrain the plane would have to do, to be at the DZ at the right time, in reverse. Additionally I had to take into account the angle of approach, and offset that with the reversed flight path. The path is calculated at the time of launching the scenario, and the terrain is moved in reverse slowly and smoothly along a bezier curve. Not too dissimilar to a clock running in reverse.

![Scenario Setup](/assets/images/pennant/VPTS_scenario_setup.png "Scenario Setup")
![In-game view of students going out](/assets/images/pennant/VPTS_jump.png "In-game view of students going out")
![Instructor View during scenario](/assets/images/pennant/VPTS_mcs_ingame.png "Instructor view during scenario")


