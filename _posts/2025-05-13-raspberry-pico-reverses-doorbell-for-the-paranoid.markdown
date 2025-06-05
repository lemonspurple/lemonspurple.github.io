---
layout: post
title:  "Raspberry Pico Reverse Doorbell For The Paranoid"
date:   2025-05-13 13:23:04 +0200
categories: update projects
---
Have you ever locked your door, only to turn back just to check if it’s really locked? I’ve done that dance a lot. Many would probably agree that the healthiest thing to do is to simply not double-check at all. After all, I’ve never actually forgotten to lock the door and my belongings are insured.
Additionally, by repeatedly choosing not to check, I can rewire my brain over time and unlearn this habit.

But what if there’s a simpler fix, assuming you don’t mind something a little neurotic? In theory, I could create a small ritual to do right after locking the door, something that would help me remember I didn’t forget. Best of all, I’d only need a microcontroller and a few LEDs.

![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/screenshot202505131428.png)

It works as follows:
You lock the door and press the button. This triggers a yellow LED that stays lit for 15 seconds. That’s just enough time for me to reach the front door of the apartment building. A quick glance over my shoulder confirms I completed the habit before heading out.
While I was at it, I added a red LED that blinks every few seconds. I figured if I’m already sticking a gadget to my door, I might as well make it look like a security device and maybe even deter intruders.

![Screencap of veins in an arm using a pi camera module, IR filter and lights.](/images/pico5280d97170d6b8.gif)

I’m still not great at C#, so I didn’t expect to do much better with MicroPython. But with some help from ChatGPT in regards to figuring out which libraries I needed and what they do, I managed to cobble together the code below.
Surely there are plenty of ways to improve it, but for now, I’m just really happy with my first microcontroller and soldering project.

{% highlight ruby %}
from machine import Pin, PWM, lightsleep
from time import ticks_ms, ticks_diff, ticks_add
import time

# Setup for LEDs
led_button = Pin(14, Pin.OUT)    # LED glows 15 seconds when button is pressed
led_dim = PWM(Pin(15))           # PWM for low glow

# PWM-Confiuguration
led_dim.freq(5000)
dim_duty = int(535 * 0.1)           

# Button-Setup
button = Pin(13, Pin.IN, Pin.PULL_UP)

# Timestamp for LED 14
led_on_until = 0

while True:
    now = ticks_ms()

    # LED on GPIO 15 short glow
    led_dim.duty_u16(dim_duty)
    time.sleep(0.2)
    led_dim.duty_u16(0)

    # Button press starts new 15 sec loop
    if button.value() == 0:
        led_on_until = ticks_add(now, 15000)

    # LED 14 on/off based on time
    if ticks_diff(led_on_until, now) > 0:
        led_button.on()
    else:
        led_button.off()

    # powersaving
    lightsleep(1800)
{% endhighlight %}

If you wanna use this code, mind the GPIO pins of your device or change them in the code.