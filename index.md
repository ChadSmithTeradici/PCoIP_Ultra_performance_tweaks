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

Part 1: Understanding your client side bandwidth
On your client system that will establishing the PCoIP connection enusre you are NOT using WIFI and using a ethernet cable on your local network. Next, check your local ISPs internet subscription plan by 

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
