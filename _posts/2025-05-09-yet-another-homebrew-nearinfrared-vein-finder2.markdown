---
layout: post
title:  "Finally, We Made It To Development Hell"
date:   2025-05-15 20:23:04 +0200
categories: update devblog
---
Despite well willing advice I set up a gamedev project. My gut says I shouldn't talk unfinished business, as blogging about it feels like some ascended form of procrastination. Since I was going to write my thoughts anyway somewhere, I figured I'd do it here for easy access.
{:refdef: style="text-align: center;"}
![Healthbar](/images/tow_alpha_43b3ae4ec5f380.gif)
{: refdef}
Today I've got basic health calculations working. Instead of just moving forward, I'm already nitpicking using GetComponent<> over FindFirstGameObjectByType<>, and still wrestling with classes, their referencing and instanting. Also wondering if I can refactor the health function to ditch the color logic from Update().

Hm.
Next are object pools. But first, the enemies need some brains. Not sure yet how the spawner will tick, I’m thinking enemies spawning in clockwise waves around the tower. Maybe a rotating cylinder with the tower as the pivot as a spawn area, so I can reuse the script. Then comes a damage function, which means I’ll need modifiable enemy instances. Graphics is something I'll be tackling as late as possible or when my brain is running on empty.

{:refdef: style="text-align: center;"}
![Healthbar](/images/tow_alpha_4b4ce8cc16648a.gif)
{: refdef}

The course I've been doing in preperation lead me through setting up a BFS pathfinding algorythm manually. If this might run more cost efficient than a NavMesh - which seems way easier to use - is something we will never find out.