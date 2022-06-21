---
title: "Gyroflow v1.1 is out!"
layout: splash
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: assets/images/banner.jpg
  actions:
    - label: "Download"
      url: "https://github.com/gyroflow/gyroflow/releases"
    - label: "Repository"
      url: "https://github.com/gyroflow/gyroflow"
    - label: "Docs"
      url: "https://docs.gyroflow.xyz/"
      class: "btn--primary"
excerpt: "Gyroflow is now faster, more intuitive, and production-grade"
intro: 
  - excerpt: "Advanced open-source gyro-assisted video stabilization for cinematography, drone videography, and much more! Bring your cinematic footage to the next level."
feature_row:
  - image_path: /assets/images/ui_picture.jpg
    alt: "Modern UI"
    title: "Modern  user interface"
    excerpt: "New and improved cross-platform user interface with realtime hardware accelerated video playback and blazingly fast video export. And yes, it comes with a dark mode."
  - image_path: /assets/images/stabexample.jpg
    alt: "Stab"
    title: "Advanced stabilization"
    excerpt: "Gyroflow corrects for lens distortion and contains a handful of customizable video smoothing algorithms, including horizon leveling, to achieve exactly the stabilized look you need."
    # url: "#test-link"
    # btn_label: "Read More"
    # btn_class: "btn--primary"
  - image_path: /assets/images/fpv_logger.jpg
    title: "Flexible workflow"
    excerpt: "Put a gyro source and a camera together and you're ready to go. Native support for gyro data from GoPro, Insta360, Sony, Runcam, Drone blackbox etc. and up to 16-bit video processing."
---


{% include feature_row id="intro" type="center" %}

<iframe width="560" height="315" src="https://www.youtube.com/embed/QR-SINyvNyI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
{% include feature_row %}
# Features ([See the repository for more information](https://github.com/gyroflow/gyroflow))

<div style="width: 100%; height: auto; margin: 0 auto;"> 
    <video loop autoplay muted style="width:47%;">
  <source src="/assets/videos/comparison1.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>
  <video loop autoplay muted style="width:47%;float:right;">
    <source src="/assets/videos/comparison2.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
    <div style="clear:both;"></div> 
</div>





- Real time preview, params adjustments and all calculations
- GPU processing and rendering
- Fully multi-threaded
- Rolling shutter correction
- Supports already stabilized GoPro videos (captured with Hypersmooth enabled) (Hero 8 and up)
- Supports and renders 10-bit videos (and higher, up to 16-bit 4:4:4, direct YUV rendering with no data loss - no conversion to RGB)
- Visual chart with gyro data (can display gyro, accel, magnetometer and quaternions)
- Visual display of smoothed quaternions
- Real time offset adjustments
- Adaptive zoom (dynamic cropping)
- Based on [telemetry-parser](https://github.com/AdrianEddy/telemetry-parser) - supports all gyro sources out of the box
- Gyro low pass filter, arbitrary rotation (pitch, roll, yaw angles) and orientation
- Multiple gyro integration methods
- Cross-platform - currently works on Windows/Linux/Mac, with Android and iOS apps coming
- Multiple UI languages
- Supports variable frame rate videos, all calculations are done on timestamps
- x264, x265, ProRes and PNG outputs, with x264 and x265 fully GPU accelerated
- Automatic lens calibration process
- Automatic updates of lens profile database
- Built-in lens profiles for GoPro HERO 6, 8, 9 and 10 in all shooting modes

# Supported formats:
- [x] Sony (a1, a7c, a7r IV, a7 IV, a7s III, a9 II, FX3, FX6, RX0 II, RX100 VII, ZV1, ZV-E10)
- [x] GoPro (All models with gyro metadata, starting with HERO 5)
- [x] Insta360 (OneR, SMO 4k, GO2)
- [x] Betaflight blackbox (CSV and binary)
- [x] Runcam CSV (Runcam 5 Orange, iFlight GOCam GR)
- [x] WitMotion (WT901SDCL binary and *.txt)
- [x] Mobile apps: `Sensor Logger`, `G-Field Recorder`, `Gyro`
- [x] Gyroflow [.gcsv log](https://docs.gyroflow.xyz/logging/gcsv/)
