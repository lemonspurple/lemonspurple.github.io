---
layout: post
title:  "Cellular Automata in C# / Blazor"
date:   2025-10-29 00:10:04 +0200
categories: projects update 
---
So, I made this [Conway's Game of Life thingy](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) that works in the console. All you need to do is run this script (trust me it's cool) on your computer. Oh! And I also need you to install dotnet runtime; it'll be only a few lines which I'll tell you exactly how to write into the terminal...  
Unfortunately, I have already maxed out the amount of tolerance I can expect from my friends for the foreseeable feature during the hat incident of 2024, which is why I had to learn Blazor to share my creation. [You can find the page here and experiment with it.](https://lemonspurple.github.io/cellularLife_blazor/)

[![Game of Life](/images/cellular_581a683bf9a911.gif)](https://lemonspurple.github.io/cellularLife_blazor/)

The main challenge for me was wrapping my head around how to render the output properly and how to navigate some common pitfalls, which you can read [all about here](https://lemonspurple.github.io/info/) in a bit more detail.  
While I still feel not as versed as I wish to be and rely on tutorials (I never did a cellular automata, this is to be expected but eh..), I felt pretty victorious when I fixed an out-of-range-exception that was caused by injecting new coordinates while the drawing process was running. All I really had to do, was write a little function that holds these values and returns them between the pausing of the game and start (i.e. when the user presses refresh). Coming up with that solution just from debug logs without googling or using ChatGPT was pretty cool; not gonna lie.
  
<br>
If the cellular muse kisses me again I might code some iterations, where you can manipulate the rules of life in more detail, color perhaps too. As is, the game scans horizontal lines, which causes a cell to spawn if hovering over a row of three. This creates so called [oscillator cells](https://en.wikipedia.org/wiki/Oscillator_(cellular_automaton)) and simultaneously raises the question what would happen if the game scans diagonally or in other patterns for me.  
One way or another, a guarantee to not grow bored. For 2026 I make the wish to spend more time on the computer and online. 
