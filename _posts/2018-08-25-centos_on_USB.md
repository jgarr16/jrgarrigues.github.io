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

_________

This first post describes the steps necessary to create a bootable thumb drive loaded with the operating system. I'll be using a Macbook Pro to download the OS and load it on the USB thumb drive because that's what I've got and this is probably the most difficult path (i.e., using Windows or Linux to do the same will likely be a little easier as there are tools available that can help out on those platforms). 

To get going, we'll gather the resources required to do the job; we're going to need: 

- A copy of the operating system.  
- USB thumb drive with sufficient capacity for your operating system.
- A computer on which to perform all of these activities (I will be using a Mac). 
- Some time... 

Before you get started, you'll need to decide which flavor of Linux you want to use. I'll be using CentOS which can be downloaded from the [CentOS homepage](https://www.centos.org). Since early June of 2018, build number 1804 is the most recent version of CentOS. I've chosen to use the "Everything ISO" (weighing in at about 9.5 GB) because I want to have the ability to use the GNOME (GUI) desktop on an as-needed basis, but you can follow these instructions with the minimal installation (for less than 1 GB) just as well. 

Once you've got your ISO image downloaded, it's time to setup the thumb drive. Do make sure that your drive is big enough to hold the ISO. The process that we'll use to write the ISO onto the thumb drive (named "dd") is time consuming and it will let you try to write to a drive that is too small which predictably results in a disk space error at the end of the long process! Save yourself the aggravation and use a drive with plenty of space. 

