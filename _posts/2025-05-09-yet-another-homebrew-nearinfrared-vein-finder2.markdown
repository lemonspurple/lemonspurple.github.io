---
layout: post
title:  "Yet Another Homebrew Near-Infrared Vein Finder"
date:   2025-05-09 15:23:04 +0200
category: [test]
---
![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/1746804975_image.png)

![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/1746804975_image2.jpg)

Been tinkering with a project that involves a NoIR camera and while I was at it I figured I might as well check out how my veins look. They become quite visible because hemoglobin absorbs IR light differently than nearby tissue. Simple post processing / decluttering methods such as contrast adjustments followed by threshold filter shows great results already (A -> B). Inversion and decluttering by gaussian blur and resharpening again (by threshold again i.E.) shows even better results. (B -> C -> D). 

Capturing images with [libcamera](https://github.com/raspberrypi/libcamera) has been... an adventure. It likes to do its own thing with automatic image correction. I’m guessing there’s a way to turn that off, probably pointed out somewhere in the documentation I didn’t read.

About the setup: Was using an RPi, NoIR camera, 850–940 nm IR pass filter, and IR lighting. Dark rooms minimizes light interference and a helping hand (tool) will save a lot of trouble.