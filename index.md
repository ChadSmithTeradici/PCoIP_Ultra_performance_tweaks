---
title: PCoIP Ultra performance tweaks
description: Learn how to fine-tune the PCoIP protocol based on your network conditions.
author: chad-m-smith
tags: Teradici, PCoIP Ultra
date_published: 2021-05-12
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This guide shows you how to fine-tune the Teradici PCoIP experience based on individual network conditions between the client and host systems. This guide is NOT intended to replace Teradicis formal [Session Planning Guide](https://www.teradici.com/web-help/pcoip_session_planning/current/tuning_session_variables/pcoip_session_variables/) but rather be a 'cliff-notes' version of the most common tweaks recommended when helping our customer get a better experience from the default settings after initial deployment. 

**Part 1: Understanding your client side bandwidth and Latency**
On your client system that will establishing the PCoIP connection enusre you are NOT using WIFI and using a ethernet cable on your local network. Next, check your local ISPs internet subscription plan by https://www.speedtest.net/

 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest1.png)
 
 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest2.png)
 
 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest3.png)
 
 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest4.png)
 
Next install a use the Teradici Session statistics viewer to see what percentage of 
 
Generally speaking, the bulk of the PCoIP traffic flows from host to client; every time the client sees missing packets, it provides feedback to the host about how many packets went missing, which the host then uses to adjust its bandwidth estimate. So if you pull up the SSV on the host and examine its logs, the loss that matters most is is the TX loss since it's relative to the host.
 
 
 **Configure the Maximum PCoIP Session Bandwidth**
 
 **Configure the PCoIP Session Bandwidth Floor**
 

Part 1: Understanding our connection
Run speed tests
Will allow you to set the "Configure Session Bandwidth Floor"
PCoIP Local GPO changes on Host/Agent System



Enable PCoIP Ultra mode > CPU offload
Enable Log Verbosity > Level 3
Image Quality settings > Set initial quality 70
Configure Session Bandwidth Floor > 100,000 (kbs)
Max PCoIP Session > 175,0


The requirement for 4;4;4 or 4:2;0 dictates the Ultra Configurations
