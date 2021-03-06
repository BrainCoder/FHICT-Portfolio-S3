# Hue 2 Nanoleaf

## Problem
In my house I have multiple smart light systems Philips hue and Nanoleaf but sadly these systems are incompatible with each other. So when I enable the main lights in my living room (Hue) my decorative lights do not turn on leaving them off most of the time.

*TLDR: I'm lazy and want to turn on/off all my incompatible smartlights using 1 remote control.*

## Plan
To solve this problem I want program an esp8266 based dev board to syncronize these systems. This involves polling my Philips hue bridge using the [[Philips Hue API]] to get the button presses of the wall switch and then using the [NanoleafAPI](https://documenter.getpostman.com/view/1559645/RW1gEcCH) to turn enable or disable my light fixtures.


## Result
A simple but effective program writen in embeded C with an aproximation of object based programming.

[Hue 2 Nanoleaf on Github](https://github.com/BrainCoder/Hue2Nanoleaf)
![[Hue2Nanoleaf 1.zip]]

## Reflection
I really enjoyed trying to use OOP style code in C and I feel like the are great benefits to trying to adhere to OOP principles in C.

