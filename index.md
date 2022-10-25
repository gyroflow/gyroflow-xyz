---
title: "Gyroflow v1.3 is out!"
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
excerpt: "Support for Hero 11, DJI Avata, BRAW, keyframing and much more!"
intro: 
  - excerpt: "Advanced open-source gyro-assisted video stabilization for cinematography, drone videography, and much more! Bring your cinematic footage to the next level."
feature_row:
  - image_path: /assets/images/ui_picture.jpg
    alt: "Modern UI"
    title: "Modern user interface"
    excerpt: "Cross-platform user interface with realtime hardware accelerated video playback and blazingly fast video export. And yes, it comes with a dark mode."
  - image_path: /assets/images/stabexample.jpg
    alt: "Stab"
    title: "Advanced stabilization"
    excerpt: "Gyroflow corrects for lens distortion and contains a handful of customizable video smoothing algorithms, including horizon leveling, to achieve exactly the stabilized look you need."
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
- GPU processing and rendering, all algorithms fully multi-threaded
- Rolling shutter correction
- Supports already stabilized GoPro videos (captured with Hypersmooth enabled) (Hero 8 and up)
- Supports and renders 10-bit videos (up to 16-bit 4:4:4:4 for regular codecs and 32-bit float for OpenEXR - works directly on YUV data to keep maximum quality)
- Customizable lens correction strength
- Render queue
- Keyframes
- Ability to create custom settings presets
- [OpenFX plugin](https://github.com/gyroflow/gyroflow-ofx) (eg. for DaVinci Resolve), which allows you to apply stabilization in video editor without any transcoding
- Visual chart with gyro data (can display gyro, accel, magnetometer and quaternions)
- Visual display of smoothed quaternions
- Modern responsive user interface with Dark and Light theme
- Adaptive zoom (dynamic cropping)
- Support for image sequences (PNG, OpenEXR, CinemaDNG)
- Based on [telemetry-parser](https://github.com/AdrianEddy/telemetry-parser) - supports all gyro sources out of the box
- Gyro low pass filter, arbitrary rotation (pitch, roll, yaw angles) and orientation
- Multiple gyro integration methods for orientation determination
- Multiple video orientation smoothing algorithms, including horizon levelling and per-axis smoothness adjustment.
- Cross-platform - currently works on Windows/Linux/Mac, with Android and iOS apps coming
- Multiple UI languages
- Supports variable and high frame rate videos, all calculations are done on timestamps
- H.264/AVC, H.265/HEVC, ProRes, DNxHD, PNG and OpenEXR outputs, with H.264 and H.265 fully GPU accelerated (ProRes also accelerated on Apple M1 Pro/Max/Ultra)
- Automatic lens calibration process
- Fully zero-copy GPU preview rendering (working but experimental)
- Core engine is a separate library without external dependencies (no Qt, no ffmpeg, no OpenCV), and can be used to create OpenFX and Adobe plugins (on the TODO list)
- Automatic updates of lens profile database
- Built-in official lens profiles for GoPro: HERO 6, 7, 8, 9, 10; RunCam: Thumb, ThumbPro, 5 Orange; Insta360: GO 2 in all shooting modes

# Supported gyro sources:

- [x] GoPro (HERO 5 and later)
- [x] Sony (a1, a7c, a7r IV, a7 IV, a7s III, a9 II, FX3, FX6, FX9, RX0 II, RX100 VII, ZV1, ZV-E10)
- [x] Insta360 (OneR, OneRS, SMO 4k, Go, GO2, Caddx Peanut)
- [x] DJI Avata
- [x] Blackmagic RAW (*.braw)
- [x] RED RAW (*.r3d)
- [x] Betaflight blackbox (*.bfl, *.bbl, *.csv)
- [x] ArduPilot logs (*.bin, *.log)
- [x] Gyroflow [.gcsv log](https://docs.gyroflow.xyz/logging/gcsv/)
- [x] iOS apps: [`Sensor Logger`](https://apps.apple.com/us/app/sensor-logger/id1531582925), [`G-Field Recorder`](https://apps.apple.com/at/app/g-field-recorder/id1154585693), [`Gyro`](https://apps.apple.com/us/app/gyro-record-device-motion-data/id1161532981)
- [x] Android apps: [`Sensor Logger`](https://play.google.com/store/apps/details?id=com.kelvin.sensorapp&hl=de_AT&gl=US), [`Sensor Record`](https://play.google.com/store/apps/details?id=de.martingolpashin.sensor_record)
- [x] Runcam CSV
- [x] Hawkeye Firefly X Lite CSV
- [x] WitMotion (WT901SDCL binary and *.txt)