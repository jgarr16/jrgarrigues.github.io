---
title: "High Sierra Display Problem"
excerpt: This post describes a resolution to problems that I encountered with my MacBook Pro after updating its operating system to High Sierra in October 2017.  
categories: tech
published: true
---

I like new stuff; software and operating systems included! I've always been eager to have the latest version of a system working on whichever device I am using at the time, to the point that I frequently run beta software to see what's coming next and help wipe out bugs and identify problems when I can. Bottom line: I think that technology is cool, but new tech is the cats' meow!

This is how I ended up installing the newest Mac operating system, High Sierra, on my mid-2015 MacBook Pro a couple months ago. As soon as I loaded it up, I was immediately confronted with an issue that I thought would be eradicated in short order because of the severity; the issue was that my (mid-2015) MacBook Pro was 'freezing up’ when I allowed it to go into sleep mode. When this happened, which was at least daily, my only recourse was to press the power button for 10 seconds to shut the computer down, then press it again for a few more seconds to start it anew. As wrong as I know it is, I tend to leave my MBP running around the clock, meaning that I frequently found it ‘frozen’ whenever I returned to the office after any period of time. 

I tried lots of things to fix this because it was driving me batty. Based on information I found on the internet, I booted it up in Safe Mode, but couldn't identify a particular application that might be causing the problem. I tried using operating system cleaning tools to no avail. I finally got to the point where I wiped my hard drive and completely reinstalled the High Sierra operating system, but there were no significant changes, so I took it a step further and did a clean install of my original OS (Yosemite), and then upgraded to High Sierra again - alas, the 'freezing' persisted! 

Up to this point, I assumed that my laptop was 'freezing up' until I ran across an article from [GottaBeMobile](https://www.gottabemobile.com/fix-macos-high-sierra-problems/). Hidden in the middle of the article is a brief mention of **fixes for display problems** which got me thinking - maybe this isn't a 'freezing' problem, but a display problem. Logically, it fit because when I restarted during hours of darkness, I could detect a faint glimmer from the display that went away when I held the power button down for 10 seconds to execute a shutdown. 

Quoting the pertinent part of the article, it says: 

> If your Mac is having problems waking from sleep or you have display problems including gray screens, blue screens or flickering images on webpages you need to take the following actions.

> <b>First reset your NVRAM.</b> Turn off your Mac. Then turn it on and hold Command+Option+P+R while the computer is booting up. You will hear two chimes or on newer MacBook Pro models you will see the screen come on and go off twice.

> <b>Now, shut your computer down again and reset the SMC [System Management Controller].</b> With your Mac off, press Shift + Control + Option and then hold these keys while pressing and holding the power button for 10 seconds.

> So far this has helped solve some of our most annoying macOS High Sierra problems.

If you follow the links in Josh's article you will find a reference to an [Apple Support post](https://support.apple.com/en-us/HT201295) about the System Management Controller (SMC). The SMC is the component that is responsible for many low-level functions on Intel-based Mac computers, such as the display. There is a link to the [NVRAM description page](https://support.apple.com/en-us/HT204063) at the bottom of the SMC page too. 

I'm only a couple days into it now, but this seems to have fixed my 'freezing' problem. So far High Sierra has waken up from its sleep state without giving me that stupid, blank screen stare and it's acting like the Mac I have come to know and love, again... My thanks go out to Josh Smith from GottaBeMobile and I hope this helps you with your issue.

FOLLOW-UP: I ran into the same issue again after installing some applications, so I'm pretty sure my issue is the result of incompatible programs...
