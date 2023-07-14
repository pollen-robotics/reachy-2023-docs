---
title: "Assemble mobile base + Reachy"
description: "Unpack safely and attach your robot correctly."
lead: "How to unpack your mobile base and attach Reachy"
date: 2022-07-16T13:59:39+01:00
lastmod: 2022-07-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "getting-started"
weight: 190
toc: true
---
## Assembly tools

You will need hex keys of size 3, 6 and 8 and a screwdriver for the assembly.

## Assembly video tutorial

Follow the instructions from the video below to learn how to aasemble the mobile base and Reachy together!

To extract the mobile base from its shipping box, we recommand to remove the wood lid and use the internal handles

{{< youtube h2MF5I29sk0 >}}  

## Turn on your robot
To power up the robot, release the emergency button and press the mobile base button (next to the mobile base's LCD screen). The mobile base's screen should turn on, indicating the current state of the battery (% remaining, current flow, etc). Then, to power up the arms and head, turn on the switch near its right shoulder.
Finally, to turn on the computer, press the button near its left shoulder. 
<p align="center">
    <video controls="controls" width="100%" muted>
    <source type="video/mp4" src="8-turn_on.mp4"></source>
    </video>
    <br>
</p>

## Understanding the power buttons and battery life good practices
The mobile base uses the 24V battery to power the wheels directly. DC-DC converters are used to generate 5V (emergency button power, USB HUB power and relay logic) and 12V for the upper body.
The 5V converter draws almost 100mA when idle and is necessary for the emergency button logic.

The emergency button and the mobile base button both need to be ON to turn on the power relay that shares the 24V with the rest of the robot. However, the mobile base button is the only one that, when turned OFF, shuts down the 5V converter.


> :warning: **WARNING!** :warning: When turning off the robot, always turn off the mobile base button to minimize the idle current consumption. If you turn off the robot with the emergency button and didn't press the mobile base button before storing your robot, the battery will deplate faster.

:bulb: Even with the mobile base button OFF, the battery screen will be powered (low consumption at around ~1mA). If you plan to store the robot for more than a month, we recommend unplugging one of the wires of the battery (like when you received the robot).


|                Configuration                | Storage time before depleting a full battery |
| :-----------------------------------------: | :------------------------------------------: |
| Mobile base button ON, emergency button OFF |                  A few days                  |
|           Mobile base button OFF            |                 A few months                 |
|           Unplugging the battery            |                 A few years                  |

