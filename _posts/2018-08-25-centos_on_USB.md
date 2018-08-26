---
title: "CentOS 7 on USB"
excerpt: Setting up a USB thumb drive with the CentOS 7 .iso image.
categories: tech
published: true
---
!["CentOS 7"](/images/CentOS.png)

This series of posts details the steps necessary to build a Linux machine out of an old Dell Latitude laptop. At a high level, the steps include the following: 

1. Build a bootable USB drive with the Linux operating system.
2. Install Linux on the laptop.
3. Install the latest version of Python
4. Enable Secure Shell (SSH) and RSync/SCP so that I can work on the Linux box remotely. 

This post starts off bydescribes the steps necessary to create a bootable thumb drive loaded with the CentOS 7 operating system. I'll be using a Macbook Pro to download the OS and load it on the USB thumb drive because that is probably the most difficult path (i.e., using Windows or Linux to do the same will likely be a little easier). So, for starters, I'll gather the resources required to do the job: 

- Operating System - I'll be using CentOS which can be downloaded from https://www.centos.org 
- USB thumb drive with sufficient capacity for your operating system.
- A computer on which to perform all of these activities (I will be using a Mac). 
- Some time... 

