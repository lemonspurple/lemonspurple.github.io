---
layout: post
title:  "Hillbilly Scanning Tunneling Microscopy"
date:   2026-01-15 00:10:04 +0200
categories: projects update 
---
Recently I dedicated a week of my vacation (plus some additional nights) to building my own scanning tunneling microscope. Since I stumbled upon [John Alexander's](https://john-alexander42.github.io/simple-stm-web-page/Disk_Scanner_Exp.htm) solution of utilizing a simple piezo disk (fire alarms and greeting cards use them to produce sound) to mount and operate the scanning tip that was later especially popularized by [Dan Berard](https://dberard.com/home-built-stm/), the idea grew on me.

[![My prototype](/images/stm_topview.jpg)](/images/stm_topview.jpg)<br>
Batteries are removed, because I don't trust my own soldering skills.

As [STMs](https://en.wikipedia.org/wiki/Scanning_tunneling_microscope) are well documented already and a stretch goal of mine is writing a full recollection of how I approached my build, I won't go as much into detail in this blog post. If you're totally unfamiliar with the technology, you can basically imagine it as a tactile microscope, although it never touches the subject, but barely makes contact which enables a phenomenon called [quantum tunneling](https://en.wikipedia.org/wiki/Quantum_tunnelling). This allows the probe to measure heights on an atomic level.

[![One of my first succesfull readings](/images/stm_reading_1.jpg)](/images/stm_reading_1.jpg)<br>
First succesful tunneling attempt.

One of the biggest challenges for me, was certainly the scattered and sometimes incomplete or contradictory documentation. Hence, my apparatus is largely based upon a combination of instructions by Berard, Alexander, the Walla Walla University and sources from the University of Regensburg.<br>
The latter holds my eternal gratitude, as they provided sources for firmware and printing my own circuit boards.<br>

[![Grid structure of a graphene sample](/images/stm_scan2.jpg)](/images/stm_scan2.jpg)<br>
[Grid structure of graphene (terrace)](https://www.google.com/search?udm=2&q=stm+graphene&dpr=1&aic=0). For comparison: a human hair is 50,000 - 10,000 nanometers thick. The atoms you can see span roughly 2nm.<br>

Looking back, I'm incredibly happy that I've thrown myself at the project (and not the project away from me. Not figuratively speaking, as there were some moments..). There were hurdles at every step of the way. For example, I didn't know how to operate one of these old rotary multimeters. I also had no idea how to solder super tiny SMD chips (surface mounted devices) let alone read circuit diagrams or even print them.<br><br>
I'm aware that it won't win a beauty contest, but it also motivates me to branch out even more and perceive learning as a hobby, something you can do for the sheer joy of it.<br>
Also, the conclusion occurred to me, that I found it easier to build a scanning tunneling microscope than to learn [co- and contravariance of C#](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/covariance-contravariance/), which I don't see as a language feature but rather a mental illness. Perhaps, however, I will improve the vibration insulation and build a case for it; there are a bunch of areas of improvement that come to mind quickly.
<br><br>
Some additional thanks:<br>
Peter Dirnhofer & Lennard Grawe for knowledge transfer. 
 I. and kadse from Chaos Compute Club Cologne for teaching/helping me to cut threads for screws.
 Tunneling Amp based on design by Jost Herkenhoff.