---
title: "Finding Reachy's IP"
description: ""
date: 2021-03-30T13:05:22+02:00
lastmod: 2021-03-30T13:05:22+02:00
draft: false
images: []
menu:
  SDK:
    parent: "getting-started"
weight: 120
toc: true
---

The last required step before actually programing your Reachy is to find its IP address. 

A small LCD screen should be installed in Reachy's back to display Reachy's IP address. You will need to take down its tee-shirt to see the LCD screen.

<p align="center">
  <img src="ip_lcd_display_reachy.jpg" alt="drawing" width="40%"/>
</p>

The instructions to display the IP address to the LCD screen is provided by the [dashboard]({{< ref "/dashboard/introduction/introduction" >}}) which is started at boot with the service [reachy_dashboard.service]({{< ref "/advanced/services/available#reachy_dashboardservice" >}}).

If the LCD screen is not working, check out the page [Find my IP section]({{< ref "help/system/find-my-ip" >}}) to learn other ways to get the IP address.

> Note: Using the SDK locally also avoids network potential latency or bandwidth issue. Yet, it may not be as convenient as working directly from your usual laptop. You need to plug a screen, keyboard and mouse directly on Reachy's computer.

You can check that everything is working as expected by running the following Python code:

```python
from reachy_sdk import ReachySDK

# Replace with the actual IP you've found.
reachy = ReachySDK(host='the.reachy.ip.found.')
```