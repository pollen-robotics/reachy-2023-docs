---
title: "Software installation"
description: ""
lead: ""
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  dashboard:
    parent: "installation"
weight: 300
toc: true
---

> Please note that the dashboard should be installed and its [main service enabled]({{< ref "/advanced/services/available#reachy_dashboardservice" >}}) by default on your Reachy.

## Clone the repository

Clone the repository reachy-dashboard from GitHub and use pip to install it.

```python
cd ~/dev
git clone https://github.com/pollen-robotics/reachy-dashboard
cd reachy-dashboard
pip3 install -e .
```
## Check Reachy's services
To be able to control [Reachy's main services]({{< ref "/advanced/services/available#services-available" >}}) with the dashbaord, the services need to be in --user mode.
To know if it is the case, in a terminal:

```bash
systemctl --user list-unit-files | grep reachy
```

## Create Reachy's Hotspot
```bash
nmcli dev wifi hotspot ifname wlp0s20f3 con-name Reachy-AP ssid Reachy-AP password "Reachy-AP"
```

## Create a service file
Create a service file so that the dashboard will be started automatically at boot along with [Reachy's main services]({{< ref "/advanced/services/available#services-available" >}}). One advantage of having this is that the dashboard will be running when you start the robot, so you won't need to plug a screen computer to Reachy nor scan the network to get its IP address and connect to it. The IP address of the robot on the network will be displayed on the [LCD screen]({{< ref "/dashboard/installation/hardware#hardware" >}}) (if you installed it). 

To create the service:

```bash
cd ~/dev/reachy-dashboard
bash setup_service.bash
systemctl --user enable reachy_dashboard.service
systemctl --user start reachy_dashboard.service
```