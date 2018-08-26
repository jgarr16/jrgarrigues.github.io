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

This post covers step one with a description of the process of creating a bootable thumb drive loaded with the operating system. 

_________

I'll be using a Macbook Pro to download the OS and load it on the USB thumb drive because that's what I've got and this is probably the most difficult path (i.e., using Windows or Linux to do the same will likely be a little easier as there are tools available that can help out on those platforms). 

To get going, we'll gather the resources required to do the job; we're going to need: 

- A copy of the operating system.  
- A USB thumb drive with sufficient capacity for your operating system.
- A computer on which to perform all of these activities (as mentioned, I am using a Mac). 
- Some time... 

### Download Operating System

Before you get started, you'll need to decide which flavor of Linux you want to use. I'll be using CentOS which can be downloaded from the [CentOS homepage](https://www.centos.org). Since early June of 2018, build number 1804 is the most recent version of CentOS. I've chosen to use the "Everything ISO" (weighing in at about 9.5 GB) because I want to have the ability to use the GNOME (GUI) desktop on an as-needed basis, but you can follow these instructions with the minimal installation (for less than 1 GB) just as well. 

The ISO file we'll be working with for the remainder of this post is "CentOS-7-x86_64-Everything-1804.iso"

### Setup USB Drive

Once you've got your ISO image downloaded, it's time to setup the thumb drive. Do make sure that your drive is big enough to hold the ISO. The process that we'll use to write the ISO onto the thumb drive (named data duplicator, "dd", and also *lovingly* called the data destroyer utility) is time consuming and it will let you try to write to a drive that is too small which predictably results in a disk space error at the end of the long process! Save yourself the aggravation and use a drive with plenty of space. 

First, we'll make the USB bootable. On the Mac, you can use Disk Utility if you want to stick with a graphical user interface, but I'm going to use the command line because it delivers much more flexibility. We start by identifying the USB drive; you can do this by running the `diskutil list` command: 

![diskutil list command](/images/diskutil_list.jpg) 

In my case, I can tell that my 64GB USB thumb drive is disk2 just by looking at the sizes. If it's close, you'll want to take additional steps to verify that you're working with the correct drive. Some of the commands we'll use here will wipe out any data you have if you use the wrong disk name or type them in improperly, so do be careful. 

Armed with the drive name, the next step will be to eject the USB drive by issuing the `diskutil unmountDisk /dev/disk2` command. If you happen to be keeping an eye on the drive in Finder, you should expect for it to disappear once you eject it on the command line. 

You don't need to, but I'm a fan of working locally whenever possible - so I will change my directory to my Downloads folder where I stored my CentOS ISO (`cd Downloads`). Because I'm doing this on a Mac, I have to convert the ISO file into a DMG image so that it will be easier to work with. We'll do this with the `hdiutil` command which is arranged as such: 

`hdiutil convert -format UDRW -o <new DMG image name> <old ISO filename>`

In my case, the actual command looks like this:

`hdiutil convert -format UDRW -o CentOS-7-x86_64-Everything-1804 CentOS-7-x86_64-Everything-1804.iso`
