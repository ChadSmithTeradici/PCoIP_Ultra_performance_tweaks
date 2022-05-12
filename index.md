---
title: PCoIP Ultra performance tweaks
description: Learn how to fine-tune the PCoIP protocol based on your network conditions.
author: chad-m-smith
tags: Teradici, PCoIP Ultra
date_published: 2021-05-12
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This guide shows you how to fine-tune the Teradici PCoIP experience based on individuals network conditions between the client and host systems. This guide is NOT intended to replace Teradicis formal [Session Planning Guide](https://www.teradici.com/web-help/pcoip_session_planning/current/tuning_session_variables/pcoip_session_variables/) but rather be a 'cliff-notes' version of the most common tweaks we recommend when helping our customer get a better experience from the default settings after initial deployment. 

Part 1: Understanding our connection
Run speed tests
Will allow you to set the "Configure Session Bandwidth Floor"
PCoIP Local GPO changes on Host/Agent System



Enable PCoIP Ultra mode > CPU offload
Enable Log Verbosity > Level 3
Image Quality settings > Set initial quality 70
Configure Session Bandwidth Floor > 100,000 (kbs)
Max PCoIP Session > 175,0
