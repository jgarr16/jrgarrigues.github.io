---
title: "CentOS GUI vs. CLI"
excerpt: Working through the ability to bounce back and forth between the command line and a graphical user interface.
categories: tech
published: true
---
I have been running CentOS on an old laptop for a little while now. I initially set it up to mimic my work environment, where I needed to work across Windows and Linux platforms to do the things I needed to do on the job. 

I started off working purely on the command line with no real need for the graphical user interface. Over time I realized that I had a need for interactivity beyond the command line; particularly when I needed to reach out and find information (usually via a web browser). Some needs I was able to solve within the confines of the textual boundaries of CLI - email using [Mutt](http://www.mutt.org), even some preliminary internet searching using [Googler](https://github.com/jarun/googler), but there were still situations that required more. 

Eventually, I ended up updating my minimal installation of CentOS to a version that enabled the GNOME graphical user interface to ensure that I could leverage the desktop when I need it. But, I don't want to go there all the time. Not even, in fact, most of the time. 



`systemctl set-default multi-user.target`

`systemctl set-default graphical.target`
