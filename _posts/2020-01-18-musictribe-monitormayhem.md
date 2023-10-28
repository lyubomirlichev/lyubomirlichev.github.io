---
title: Monitor Mayhem
date: 2020-01-18
categories: [Music Tribe]
tags: [Windows, VR, Simulation, Gameplay, HTC Vive, Unity]
pin: true
---

### Project description
Planned, designed, and implemented UI and features of a VR research/game experience for Monitor Engineers. The aim of the experience is to supplement research done by University of Birmingham, on the immersive benefits of VR in stressful situations. Can we put the user in a stressful situation where they forget they are wearing a headset and feel truly present ? Can we do this in an engaging and fun way ? I worked as part of a team to deliver the Monitor Mahyem experience, and we achieved all of the above.

Trailer:

[![Image alt text](https://img.youtube.com/vi/3H3N3wM3pHc/0.jpg)](https://www.youtube.com/watch?v=3H3N3wM3pHc)

### What I worked on
- I worked on extending, improving, and fixing, an underlying Content Management project system for producing various demos, concepts, and uncategorized applications. This system allowed us to have an efficent art and code workflow. In essence, the visual assets of the experience are bundled separately into Asset bundles. Those Asset Bundles are shared on a on-premises server. The application that gets installed serves as a client, only containing functionality, not assets. Upon launching the application, all assets are downloaded and prepared. This allowed us to have much shorter artwork iteration time, feature development, testing, and releasing. The system was comprised of:
  - Environment Manager, which manages and bundles Unity scenes.
  - Catalogue Manager, which manages and bundles individual assets.
  - Fully integrated CI/CD, used to build all of this on an Azure DevOps service remotely.
- I worked on implementing and working closely with Design on the UI, including but not limited to:
  - The console menu controls, animations, input, interactions.
  - The floating Orders UI and Order Details UI, comprised of custom shaders, animations, assets, prefabs and more.
  - The phase of the experience where the user is tasked which checking off all of their tools.
- Testing, bug fixing, CI/CD maintenance, releasing, demos.
