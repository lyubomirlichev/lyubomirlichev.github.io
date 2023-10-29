---
title: Gatherings VR
date: 2021-03-23
categories: [Mesmerise]
tags: [Meta Quest, VR, CMS, UI, Unity]
pin: true
---

### Project description
[Gatherings](https://gatheringsvr.com/support/) is an always on persistent world where you can explore, watch and connect. 
The application allows a VR user to experience a shared space with their colleagues, have meetings, attend events, and explore digital activities.
The application runs on a Unity-based platform, with Azure backend, and Unity frontend. The entire content of the app is delivered in real time, on demand, as part of a platform-level CMS system, using Asset Bundles.

Over three years, Gatherings grew and adapted in numerous ways, taking advantage of new technologies in a rapidly expanding market. Evolving a product that was originally a single user experience, to persistent ecosystems with impressive capabilities to support over 100 users in a single space.

Initially, I was a mid-level software engineer, tasked with implementing and improving the immersive spatial UI. I collaborated closely with the design team and other engineers, to implement a smooth seamless front-end experience, powered by a data-intensive platform.

After the public release of Gatherings, I was moved up to Senior-level, and became part of the team tasked with re-developing and deploying a fully comprehensive CMS system. This new system with a Unity extension front-end afforded the art team with rapid construction of VR spaces. The CMS system supported updating spaces, assets, templates and much more. 
[GatheringsVR on Quest Store](https://www.meta.com/en-gb/experiences/3620763894706423/).
### What I worked on
- [Personal Menu](https://vimeo.com/567129910)
  
<img width="394" alt="image" src="https://github.com/lyubomirlichev/lyubomirlichev.github.io/assets/74913022/5a89e91a-8b6c-4dd6-9afc-06bd69a4687b">

I worked closely with the Design team to implement an extendable and scalable VR-optimized menu framework, and was responsible for the following:
  - The ability travel between spaces: As the application acts as a client, all of the data needed for spaces is retrieved on demand, through the Spaces tab. I implemented custom scroll view system which only showed 10 unique items at a time but simulated an infinite scrolling functionality. The menu also takes into account that each space has dependencies in the form of asset bundles, which have to be validated or downloaded before a user can join a space. The spaces tab included multiple categories of spaces, minimal latency, near-instant loading of custom thumbnails, all in less than 30 draw calls.
  - The ability to search for spaces: I designed and implemented a custom search functionality to help the users find the space they are looking for quickly. This included sketching designs, finding the right placing for a search bar, the right user interactions, the most optimal search algorithm for this context, and more.
  - As the menu can be opened by the user anywhere at any time, I implemented a system which dynamically positions the menu at the right height and distance relative to the user's position and direction. The menu will always open up in-front of the user, regardless of their set up. Example can be found [here](https://github.com/lyubomirlichev/PersonalExamples/blob/main/Assets/Scripts/Orbiter.cs).
  - Many tweaks, extensions, bug fixes, adjustments.

In addition to the Personal Menu, some of my other contributions to the project were:
- Completely redesigned and updated VR keyboard (video [demo](https://vimeo.com/567142326))
  - <img width="394" alt="Keyboard" src="/assets/images/mesmerise/keyboard.jpg">
- Implemented fully configurable and VR-optimized Tutorial (video [demo](https://youtu.be/Am5g2oxsG4s)) and configurable tutorial sequence.
  - <img width="394" alt="Tutorial" src="/assets/images/mesmerise/tutorial_components.png">
- Implemented a mechanic to allow the user to express reactions using input form their VR controller's thumbstick. The reactions can then be seen by other users in the space.
  - <img width="394" alt="Reactions" src="//assets/images/mesmerise/reactions.jpg">
- Implemented fully async loading system for the application, broken up into separate independent stages. The application's loading time was reduced by about 40 seconds just through the benefit of having separate loading stages instead of everything being spaghetti. Example can be found [here](https://github.com/lyubomirlichev/PersonalExamples/blob/main/Assets/Scripts/StagedLauncher.cs).


After the release of Gatherings, I worked on a full refactor of the CMS system which powers the experience. This included designing and implementing Unity Editor UI window, which allowed artists to author, modify, delete content completely independently from the client application. For example and artist can set up a space using one of the templates, populate it with assets, and publish it in just a few minutes, all from this Editor Window. Content included : Spaces, Catalogue items, Templates, Layouts, and more.

This update to the CMS system completely overhauled the Gatherings application and it's underlying platform, as now the data powering it could be managed easily from the Unity Editor. Artists could see the result of their work in-headset without being dependent on the Gatherings application's release Process. Complex, elaborate spaces and experiences could be assembled and published in under an hour.



