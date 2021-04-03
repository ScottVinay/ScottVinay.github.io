---
layout: post
title:  "Automatic crossbow"
tags: raspberry-pi woodworking
sidebar: true
text: true
description: Controlling a crossbow with a Raspberry-Pi, a servo, a button, and a sensor.
image: /assets/images/projects/crossbow/main2.jpg
---

<a href="https://github.com/ScottVinay/Crossbow">View source on Github</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/_tbwTtHWFOE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<br>

## What is it?

This is a more modern version of a home-defence system I build from a Nerf gun at university. 
The crossbow is technically a toy, but it is uses tension in the bow like a real crossbow rather than elastic cord like most toys, so it is actually quite powerful. The base is a few pieces of wood I sawed up and glued together.

## Function

The device can either be powered by USB or from the battery pack (in black, just above the RPi). However, it seems to struggle to draw enough power to operate the sensor when using battery power, so it just defaults to using the button in this case.

When the device is powered on, the sensor checks the distance to the nearest object by making a few measurements over a couple of seconds, then taking the median measurement. The green light is on during this time (although it is faint, and can't really be seen in the video). After this, whenever the distance measured by the sensor is 0.25 of the resting distance (this can be changed) or the big red button is pressed, a signal is sent to the servo arm, which rotates to pull the trigger of the crossbow.

## Components

The brains of the operation is a Raspberry Pi Pico. This is RPi's answer to the Arduino - a super cheap microcomputing chip, coming in at only £3.60, or £6 if like me you're lazy/clumsy and want the header pins to come pre-soldered. Unlike the other RPi's, this one isn't a fully-featured Linux computer. When it is powered on, it looks for any file called `main.py/main.c`, then runs that (using either Python or C). My code for this is on my Github. I found that physical microcomputing is the perfect place to use classes, since each class can correspond to a physical device. The wiring can kind of be figured out from the diagrams below, but I'll likely upload a circuit diagram sometime too.

The remaining picture shows the ultrasonic sensor. This could be a little bit tempermental. There are also the LEDs to show when the device is preparing or on standby,

<figure>
<img src="/assets/images/projects/crossbow/main2.jpg" />
<figcaption></figcaption>
</figure>

<figure>
<img src="/assets/images/projects/crossbow/sensor.jpg" />
<figcaption>Ultrasonic sensor</figcaption>
</figure>

<figure>
<img src="/assets/images/projects/crossbow/rpi.jpg" />
<figcaption>Raspberry Pi Pico</figcaption>
</figure>