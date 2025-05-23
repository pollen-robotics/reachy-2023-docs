---
title: "Turn on your robot"
description: "How to turn on your robot."
lead: "How to turn on your robot."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "getting-started"
weight: 210
toc: true
---

## Full/Starter kit

Connect the power supply to the robot (g) placement on the [robot back interface]({{< ref "full-kit#reachys-hardware-interface" >}}).  

Orbita neck needs to start in a straight position for its initialization. To do so, position the head so that Reachy looks straight ahead. (Don’t worry, the position doesn’t need to be exact, it just has to be correctly oriented).  

You have two buttons behind the robot:
- (a) : turn on/off Reachy’s embedded computer
- (h) : turn on/off alimentation of Reachy’s motors

{{< alert icon="👉" text="Turn on the motors with button (h) before starting the robot using button (a)." >}}

| 1. Position the head so that Reachy looks straight ahead | 2. Switch on the motors | 3. Turn on the robot |
| -------|-------------|----------|
|{{< img class="img-table" alt="Reachy's base fixation" src="look-straight.jpg" width="20%" >}}|{{< img alt="Reachy's base fixation" src="button-h.png" width="40%" >}}|{{< img alt="Reachy's base fixation" src="button-a.png" width="40%" >}}|


## Arm kit

Plug the power supply on your arm on element (1):

<p align="center">
<img src="plug-in.jpg" alt="drawing" width="40%"/>
</p>

The led should turn red.  

Connect directly the the [USB2AX board](https://www.seeedstudio.com/USB2AX-p-1349.html) to your computer and you should be good to go! The USB2AX board should be connected with a three wires Dynamixel cable to the power supply board as well.

<p align="center">
<img src="arm_kit_usb2ax.jpg" alt="drawing" width="40%"/>
</p>