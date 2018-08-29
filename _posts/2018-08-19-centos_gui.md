---
title: "CentOS GUI vs. CLI"
excerpt: Working through the ability to bounce back and forth between the command line and a graphical user interface.
categories: tech
thumbnail: wrench
series: CentOS
published: true
---
!["CentOS 7"](/images/CentOS.png)

I have been running CentOS on an old laptop for a little while now. I initially set up a lab that mimicked my work environment, where I needed to work across Windows and Linux platforms to do the things I needed to do on the job. As time went by, I found myself expanding my little lab at home and branching out beyond what was available to me in the office.

I started off working purely on the command line with no real need for the graphical user interface. Over time I realized that I had a need for interactivity beyond the command line; particularly when I needed to reach out and find information (usually via a web browser). Some needs I was able to solve within the confines of the textual boundaries of CLI - email using [Mutt](http://www.mutt.org), even some preliminary internet searching using [Googler](https://github.com/jarun/googler), but there were still situations that required more. 

Eventually, I ended up updating my minimal installation of CentOS to a version that enabled the GNOME graphical user interface to ensure that I could leverage the desktop when I need it. But, I don't want to go there all the time. Not even, in fact, most of the time. 

It quickly became apparent that there's a difference between working purely on the command line and working in a terminal window on the desktop. I could just deal with it, but a lot of the time I spent on my CentOS machine wasn't actually ON the CentOS machine - instead I was logging in remotely through a secure shell (SSH) session from my Mac or even my iPad/iPhone -the former could handle sessions for a remote desktop, but my mobile devices would be hard pressed to work well with the GUI. Seeing as how this is a NIX environment, I was confident that I could bounce between CLI and GUI; all I needed to do was figure out which commands to run to flip the GUI/CLI switch...

As it turns out, there are two. I've got the CentOS machine set to boot up to the command line, so that's my starting point. When I need to change this, I can alter the system control target (or runlevel) by entering this command:

`systemctl set-default graphical.target`

Doing so effectively puts CentOS in GUI mode (what was formerly known as "runlevel 5"). At this point I'll be running a full desktop. I can stay in that mode if I'm working locally, or I can go back to the command line evironment by entering the following command: 

`systemctl set-default multi-user.target`

Voila! After a brief pause, I'm transported back to my familiar command line environment where I can try to get something done without those pesky GUI distractions! 
