---
title: PCoIP Ultra performance tweaks
description: Learn how to fine-tune the PCoIP protocol based on your network conditions.
author: chad-m-smith
tags: Teradici, PCoIP Ultra
date_published: 2021-05-12
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This guide shows you how to fine-tune the Teradici PCoIP experience based on individual network conditions between the client and host systems. This guide is NOT intended to replace Teradicis formal [Session Planning Guide](https://www.teradici.com/web-help/pcoip_session_planning/current/tuning_session_variables/pcoip_session_variables/) but rather be a 'cliff-notes' version of the most common tweaks recommended when helping our customer when they are experiencing high latency, low bandwidth and dropped packets and changes from the  from the default settings are required.

This guide will be divided into three sections that correspond to the data points that will be collected. Finally all these values will be plugged in a PCoIP tuning setting to ensure the communications between the host and client are optimized. 

**Part 1: Understanding your client side bandwidth and latency**
On your client system that will establishing the PCoIP connection enusre you are NOT using WIFI and using a ethernet cable on your local network. Next, check your local ISPs internet subscription plan by https://www.speedtest.net/. This setting will provide your connection ceiling, understanding in the below example that you will never exceed ~75Mbs download and ~11Mbs upload from your local service provider. It is recommended you run several test and calculate a average download and upload number. 

 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest1.png)
 
 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/SpeedTest2.png)
 
 
 **Part 2: Seeing if there are any dropped packets**
 
The bulk of the PCoIP traffic flows from host to client; every time the client sees missing packets, it provides feedback to the host about how many packets went missing, which the host then uses to adjust its bandwidth estimate. When adjusting the session bandwidth value  you can hard-code to accommodate for any dropped packet, if you are experiencing it. 

To gather this information, we will use the health monitor feature built into the PCoIP client which requires 23.01 client release. You will need to keep your eye on the dropped packets number. If you experience any number greater than 2% you should leave a bandwidth buffer by lowering your bandwidth number by 10%. 

 ![image](https://github.com/ChadSmithTeradici/PCoIP_Ultra_performance_tweaks/blob/main/images/Health_Connection.png?raw=true)
 
 **Configure the Maximum PCoIP Session Bandwidth**
 
 Specifies the maximum bandwidth, in kilobits per second, in a PCoIP session. The bandwidth includes all imaging, audio, virtual channel, USB, and control PCoIP traffic. Setting this value prevents the agent from attempting to transmit at a higher rate than the link capacity, which would cause excessive packet loss and a poorer user experience. 
 
 For more information on the specific PCoIP Host setting review the variable setting page in the [administration guide](https://www.teradici.com/web-help/pcoip_agent/graphics_agent/windows/22.09/admin-guide/configuring/configuring/#maximum-pcoip-session-bandwidth).
 
As a general rule you want to take your bandwidth number (minus 10%) then enter that number as Max PCoIP Session bandwidth number in kbit/s
See UnitConverters url; Convert Mbps to Kbps (unitconverters.net)

In our example we have ~70mbp/s -10% = 63mbps (6451.2 kbit/s)

 **Configure the PCoIP Session Bandwidth Floor**
 
 Understanding our connection Run speed tests Will allow you to set the "Configure Session Bandwidth Floor" PCoIP Local GPO changes on Host/Agent System.
 
 For more information on the specific PCoIP Host setting review the variable setting page in the [administration guide](https://www.teradici.com/web-help/pcoip_agent/graphics_agent/windows/22.09/admin-guide/configuring/configuring/#pcoip-session-mtu).
 
-	The assumption that you will only be consuming bandwidth just for the PCoIP session and not be using the any other applications that utilize your bandwidth. 
-	You can use the same number in Max PCoIP session bandwidth setting if you aren't expereince any dropped packets, if you are you should take an additional 10% off the Maximum PCoIP Session Bandwidth number. 

**Set initial quality**

If you are expereincing a long-haul (high latency) with dropped packet on your connection betwenn client to host, it is best to lower the initial quiality down from the default of 80 to 70 to accomdate a network conditions. If your connection IS NOT expereincing any dropped packets leave at 80. 

 For more information on the specific PCoIP Host setting review the variable setting page in the [administration guide](https://www.teradici.com/web-help/pcoip_agent/graphics_agent/windows/22.09/admin-guide/configuring/configuring/#pcoip-session-mtu).
 
