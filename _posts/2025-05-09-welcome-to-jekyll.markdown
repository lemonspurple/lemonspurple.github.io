---
layout: post
title:  "Yet Another Homebrew Near-Infrared Vein Finder"
date:   2025-05-09 15:23:04 +0200
categories: update projects
---
![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/1746804975_image.png)

![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/1746804975_image2.jpg)

Simple decluttering methods such as contrast adjustments followed by threshold filter shows great results already (A -> B). Inversion and decluttering by gaussian blur and resharpening again (by threshold again i.E.) shows even better results. (C -> D). 

Using [libcamera](https://github.com/raspberrypi/libcamera) as software for captures has been a bit of a hassle, especially as image-correction happens autonomously. I wouldn't be surprised if this can be adjusted and/or disabled manually, if the documentation is consulted.

Using an RPi, NoIR camera, 850–940 nm IR pass filter, and IR lighting, veins become visible because hemoglobin absorbs IR light differently than nearby tissue. Dark rooms minimizes light interference and a helping hand (tool) will save a lot of trouble.