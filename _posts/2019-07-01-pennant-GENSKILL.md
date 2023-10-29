---
title: AR quiz for Generic Hand Skill Trainer
date: 2019-07-01
categories: [Pennant]
tags: [AR, Mobile, iOS, Android, UWP, Windows, Unity]
pin: false
---

### Project description
The Generic Hand Skills Trainer, regularly referred to as GenSkill is a free standing physical representation of a typical Flying Control Run. The GenSkill provides training in the hand skills necessary to work on aircraft components in confined spaces through access panels in an aircraft fuselage. I was involved in producing a Quiz AR app to supplement the main training procedure. 

[Details](https://www.pennantplc.com/generic-hand-skill-trainer-genskill-mk2-2/)

[More details](https://www.pennantplc.com/new-product-launch-genskill-mk2/)

{% include embed/youtube.html id='KZao4Ei4tRM' %}
### What I worked on
The Quiz application's purpose was to test the student's recognition of faults on the hardware. I implemented the entire system using Unity 3D and Vuforia. The Application runs on Android tablet, iPad, and Windows tablet.

Screenshots not available.

How it works:
- The instructor prepares the test by placing various QR code anchors along the GenSkill - the physical free standing physical representation of a typical Flying Control Run. 
- The QR codes serve as anchors' detected by the AR app when the quiz begins.
- The AR app is started on the tablet, and the student's details are entered.
- The Quiz is started, and the AR app transitions to AR mode. The student is prompted to point the camera at the QR anchors.
- Upon anchor detection, a 3D model of a wiring loom appears. This 3D model has a random subset of assets, representing faults. For example - slightly torn on the corner, twisted in the middle, cut through at the end, etc.
- The Student observes the 3D model, and answers a series of multiple choice questions that appear on the bottom of the device's screen.
- The Quiz ends, and displays the student's results for the instructor to assess.

