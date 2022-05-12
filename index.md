---
title: PCoIP Ultra perforamnce tweaks
description: Learn how to fine-tune the PCoIP protocol based on your session latency and requirements.
author: chad-m-smith
tags: Teradici, PCoIP Ulta,
date_published: 2021-05-12
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This guide shows you how to install Teradici PCoIP agent on a Mac instance running in AWS. Also, this guide is intended for customers that have Teradici annual subscription and are interested in transferring licensed seats to a AWS EC2 MAC instance(s). There is an alternative option for a AWS marketplace hourly subscription which doesn't coincide with EC2 Mac instance 24hr minimum allocation period, AWS marketplace offering is NOT a part of this deployment guide.

EC2 Mac instances are available for purchase as Dedicated Hosts through On Demand and Savings Plans pricing models. Billing for EC2 Mac instances is per second with a 24-hour minimum allocation period to comply with the Apple macOS Software License Agreement. Through On Demand, you can launch an EC2 Mac host and be up and running within minutes. At the end of the 24-hour minimum allocation period, the host can be released at any time without further commitment. 

More Information on EC2 MAC Instance can be found [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-mac-instances.html).
