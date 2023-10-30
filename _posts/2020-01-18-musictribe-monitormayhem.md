---
title: Monitor Mayhem
date: 2020-01-18
categories: [Music Tribe]
tags: [Windows, VR, Simulation, Gameplay, HTC Vive, Unity]
pin: false
---

Monitor Mayhem is a VR experience aimed at testing the immersive properties of VR in the form of a stressful environment.

The aim of the experience is to supplement research done by University of Birmingham, how immersive VR is in relation to a stressful scenario. Can we put the user in a stressful situation where they forget they are wearing a headset and feel truly present ? Can we do this in an engaging and fun way ? I worked as part of a team to deliver the Monitor Mahyem experience, and we achieved all of the above. The experience provides a scenario in which the player is the recipient of rapid and unexpected demands and tasks of the performing band. The player must use the provided tools and console to fulfil those tasks before it's too late.

Trailer:

{% include embed/youtube.html id='3H3N3wM3pHc' %}

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
