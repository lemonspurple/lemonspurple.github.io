---
layout: post
title:  "(DevBlog) Buying Copium In The Unity Asset Store"
date:   2025-09-13 02:10:04 +0200
categories: update devblog
---
A very buggy, but rudimentary proof of concept of a lobby is working. [This might sound a bit like a déjà vu](https://lemonspurple.github.io/update/projects/2025/08/07/concussion-leading-to-multiplayer-framework-evaluation.html), but the last iteration had so many different code components flying around that it was becoming increasingly difficult to work on.
On Friday I tried to essentially plug this system into a session browser, which broke the project in so many fascinating ways that I had to roll back the entire progress a few hours (thanks Git). Somehow, however, even after rebuilding, some changes in the scene data weren't backed up and I had to revert my changes by hand (thanks Git), which led me to the idea of setting up a "new project" and just do a vertical slice as a proof of concept that wouldn't contaminate the rest of the game.

![The session browser](/images/Screenshot_20250913_112611.png)

Well, now we can basically join and host a room in three different regions. When I do so, the list is auto-updated and shows rooms available rooms. On top of that (or on bottom) there are also filters that I can use to sort by name and region. Although the list updates very quickly, I added a refresh button, so you have something to do while the person who said is going to host is in the bathroom.

My favorite part was when ChatGPT suggested that I try the Unity Multiplayer Play Mode™. 
When testing, you usually build your game and upload it to itch.io to make sure that everything is working. This takes a minute or two every time and is a bit repetitive and annoying. So, instead, this handy little package promises to allow multiple instances of the game, making these steps redundant.
After importing this tool, the prototype became immediately unusable, because importing it disables http connections entirely in a Unity user config. Imagine my joy upon discovering that out after removing the package didn't fix it at first.
I suppose, knowing now that my multiplayer framework requires this to send out some pings to their servers, I could disable the disabling, however, after trying to make sense of this for two nights, I wasn't really feeling very experimental anymore.

![Picture illustrating my workflow](https://live.staticflickr.com/65535/54753285619_a719659f6e_b.jpg)

This leaves me at a crossroads. Perhaps or perchance, I should just buy a prototype from the asset store and move on with my life, building the actual game by ripping out the demo and replacing it with my own game. Downside is that I also purchase code and an architecture I may not understand or be able to easily maintain. Then again, I do not understand large parts of my code after a while and using ChatGPT as an assistant to make sense of it all and to give me pointers is not too different from following someone else's code blindly.
Reminds me a bit of something I overheard programmers saying: "I'm planning to not rely on AI as much anymore" followed by "So you're back to googling?".

TL;DR: As of now, I think it would be best to just give the lobby I built a try, even if it costs me more resources than just buying an off-the-shelf solution. Implementing photons multiplayer network into unity was a task for an entire week, if not more. Now it took me two hours maybe. That's a lot of progress when you consider that I never really coded before September last year. So, while it slows the game, it speeds up my learning curve. Hopefully.
