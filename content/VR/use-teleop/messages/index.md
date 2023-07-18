---
title: "Teleoperation messages"
description: ""
lead: "Understand warning and error messages"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  VR:
    parent: "use-teleop"
weight: 643
toc: true
---

During Reachy teleoperation, several messages can show up in front of view.  

**Warning messages**  

Some messages are just **warnings**, signaling you the quality of teleoperation may be altered or the current state of the robot may evolve into future errors (motors heating up or low battery). These messages are displayed on a **dark grey background**.  
When possible, please consider acting to prevent these warnings from becoming errors.

**Error messages**  

Other messages may signal **errors**, which will lead to a fast dysfunction of the teleoperation. These messages are to take into account quickly, as you may not be controlling the robot properly anymore when they appear. These messages are displayed on a **red background**.  

{{< warning icon="👉🏾" text="When error messages appear, <b>stop teleoperation</b> and act conquently to protect your robot. " >}}
