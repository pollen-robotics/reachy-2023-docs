---
title: "Check which motors are connected"
description: ""
date: 2021-03-30T13:05:22+02:00
lastmod: 2021-03-30T13:05:22+02:00
draft: false
images: []
menu:
  help:
    parent: "system"
weight: 300
toc: true
---

Reachy's SDK Server might not work due to a motor that have been disconnected during transportation or manipulation. Knowing which motors are actually detected by Reachy's software is really useful for debug.


## Running the discovery

You can run the discovery python script to detect the connected motors. 

**Make sure that the motors are turned on using the power switch in Reachy's back**.

In a terminal, use the command: 

```bash
reachy-discovery
```

This python script will look at each robot's part (e.g head / left arm / right arm for a Reachy full kit or head / right arm for a Reachy starter kit right) and tell which motors it sees. This is useful to check whether there are missing motors, **most likely due to a disconnected cable**.

## Analysing the discovery's output

*reachy-discovery* will output each motor that has not been detected. There are four types of device that could be missing:

### Motors

You might be told that one or multiple motors seem to be missing. Usually it is due to a disconnected cable (it might happen during transportation or manipulation). You can refer to the schematic below to identify where are located the missing motors.

<p align="center">
  <img src="reachy_full_annoted.png" alt="drawing" width="80%"/>
</p>

Check the page on [How to reconnect a motor]({{< ref "help/system/reconnect-motor" >}}) if you have any missing motors. For an arm, you should focus on the first motor in the chain missing (the one with the lowest id). Because each motor is connected to the next one sequentially, if one motor is missing, the following in the chain will be as well.
For example, if you're being told that the motors *l_wrist_pitch* (id 25), *l_wrist_roll* (id 26) and *l_gripper* (id 27) are missing, it is probably there is a disconnected cable between *l_wrist_pitch* and the motor before it in the arm's chain i.e. *l_forearm_yaw*.

### Force sensor

There is one force sensor in each Reachy's arm, located between the gripper and wrist_roll motors. The id *'40'* is for the left arm's load sensor and the id *'50'* is for the one in the right arm.

If you don't see in the discovery a load sensor for an arm, it means that the electronic card used to interact with the force sensor and which is placed around the arm's effector is not detected.

The location of this board is shown below.

<p align="center">
  <img src="load-sensor-gripper.jpg" alt="drawing" width="50%"/>
</p>

### Fans board

For each arm, there is a board used to control Reachy's fans called *r_fan* for the right arm and *l_fan* for the left arm. If either of them is missing, it means that there might be a connection issue with the card.

<p align="center">
  <img src="fan-board.jpg" alt="drawing" width="50%"/>
</p>


### Orbita

The last element that you should see if you have a Reachy with an head is the Orbita joint of the neck. If you don't see it, check that the actuator is actually powered, there should be a red led on as shown below.

<p align="center">
  <img src="orbita-led.jpg" alt="drawing" width="50%"/>
</p>

## Redoing a discovery

Doing a new discovery after each cable manipulation for devices will allow you to check if the problem is solved.

> :bulb: Don't forget to turn off and then back on Reachy's motors using the switch in its back before redoing a discovery!

## Restarting the service

Once you have all the motors and load sensors you need in the discovery, you can restart Reachy's software.

```bash
systemctl restart --user reachy_sdk_server.service
```
