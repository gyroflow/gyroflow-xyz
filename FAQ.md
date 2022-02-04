---
layout: single
title: FAQ
---

## Something doesn't work
Start by consulting the [docs](http://docs.gyroflow.xyz/) and asking in the [Discord server](https://discord.gg/BBJ2UVAr2D).

## Will this work with a GoPro Hero 5/7 on a drone
Hero 7 should work fine with Gyroflow for handheld footage, but has fundamental (hardware?) issues with gyro noise and aliasing, so motion data is essentially lost when hardmounted on a drone due to the vibrations. You can use softmounting e.g: [https://www.thingiverse.com/thing:3842261](https://www.thingiverse.com/thing:3842261) or use an external gyro source.

Something similar is the case for the SMO4k, which also has noisy motion data.

## How does gyro-based image stabilization work?
Classic video stabilization methods work by estimating the camera motion using optical flow, but this involves "guesswork" so to speak.
MEMS gyroscopes can be used to determine the rotation of the camera very accurately. The first step is to sync the gyro and the video. Then a virtual camera can be created that moves just like the physical camera, which "projects" the image onto an imaginary plane or sphere. Another (smoothed) camera can recapture the view, resulting in a stabilized video. In practice the projection and recapture can be combined using some fancy mathematics. 

This [companion video](https://youtu.be/I54X4NRuB-Q) to the the paper _Digital Video Stabilization and Rolling Shutter Correction using Gyroscopes_ by Karpenko et al. explains the basic concepts quite well. 

## There is no lens profile for X. What do I do?
Create a new lens profile by following the guide. It only takes a few minutes. If it works well, please submit it to be added as a default profile so others can use it.
Since you can add a name to the profile, future users can tell who the awesome calibrator was.

## I tried out a lens profile for my camera, but it doesn't work very well?
Try making a new lens profile to see if that helps. If it works better, please submit the new profile as well. Bad lens profiles typically move too much or too little during panning or tilting, and has "wobbling" at the edges.