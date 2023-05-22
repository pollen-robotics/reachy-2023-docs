---
title: "Applications"
description: "Dashboard page to control Reachy's applications."
lead: ""
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  dashboard:
    parent: "content"
weight: 240
toc: true
---
The page applications is dedicated to the autonomous applications installed for Reachy. 

Having this page is useful to control start some autonomous application for Reachy easily.

## Content

In this page, one card will be created per Reachy's application. Typically the page will looks like the following:

<p align="center">
  <img src="services.png" alt="Services page" width="100%"/>
</p>

For each application, it will be indicated whether the application is currently running or not and three buttons will be available:
* **Restart**: restarts the application,
* **Stop**: stops the application,
* **Show logs**: displays the logs of the application. Having the logs is useful for debugging, you will be able to see the error messages on what is causing the problem as if you were launching Reachy's code in a terminal.

> :warning: :warning: Be careful not to start multiple applications at the same time!

Currently, only two autonomous applications are available: [Hello world]({{< ref "/sdk/application/hello-world" >}}) and [Face tracking]({{< ref "/sdk/application/face-tracking" >}}).

## Notes
:bulb: If you want to developp your own Reachy's application and be able to control it on this page, you will have to define a service starting your application. The service name shoud start with *app_reachy_* --user mode.
Check the repository of the [Hello world](https://github.com/pollen-robotics/hello-world) and [Face tracking](https://github.com/pollen-robotics/reachy-face-tracking) projects to learn how to build such applications.