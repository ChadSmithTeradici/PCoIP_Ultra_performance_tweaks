---
title: PCoIP Ultra performance tweaks
description: Learn how to fine-tune the PCoIP protocol based on your network conditions.
author: chad-m-smith
tags: Teradici, PCoIP Ultra
date_published: 2021-05-12
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This guide shows you how to fine-tune the Teradici PCoIP experience based on individuals network conditions between the client and host systems. This guide is NOT intended to replace Teradici formal [Session Planning Guide](https://www.teradici.com/web-help/pcoip_session_planning/current/tuning_session_variables/pcoip_session_variables/) but rather be a 'cliff-notes' version of the most common tweaks we recommend when helping our customer get a better experience from the default settings. 

EC2 Mac instances are available for purchase as Dedicated Hosts through On Demand and Savings Plans pricing models. Billing for EC2 Mac instances is per second with a 24-hour minimum allocation period to comply with the Apple macOS Software License Agreement. Through On Demand, you can launch an EC2 Mac host and be up and running within minutes. At the end of the 24-hour minimum allocation period, the host can be released at any time without further commitment. 

More Information on EC2 MAC Instance can be found [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-mac-instances.html).
