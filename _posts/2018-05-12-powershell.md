---
title: "Customizing Powershell"
excerpt: I find myself using Windows Powershell more and more these days; wanted to customize the experience.
categories: tech
thumbnail: wrench
published: true
---
!["Windows Powershell!"](/images/powershell2.png)

It has been known by various names over the years - dos prompt, command line, cmd - but now, it's Powershell. Personally, I prefer to work in nix environments, but I don't always get a choice when I need to do something on the command line at work. So, Powershell it is... And Powershell is actually a pretty decent product; it has come a long way - it's even open source now!  

!["Windows DOS Prompt"](/images/win95dosprompt2.png)  

The name has changed, but its looks haven't. At least, not on the face of it. Powershell's out-of-the-box appearance isn't much different from the original; black background, white text, plain Jane. The saving grace is that you can modify its appearance to your personal preferences; that's what we're going to do here. 
The first step is pretty simple. Open up the Powershell application, right-click the top bar of the window and select __Properties__. 

!["Powershell configuration"](/images/powershelloptions3.png) 

Play around with the colors for the background, text, even the opacity of the window itself. Once you've found the right combination, consider doing the same on the __Default__ tab. 
With the initial configuration out of the way you will be straight on the basics, but you're going to find that there are still a few tweaks you want to make. Unlike the first part, these are a little more advanced and can't be done in the graphic user interface (GUI). Fittingly, they have to be made in Powershell itself. 
 
Open a PowerShell window and type in the following command `$host.privatedata`.
You'll be presented with the color schema for some additional components that looks something like this: 

```
    ErrorForegroundColor    : Red 
    ErrorBackgroundColor    : Black 
    WarningForegroundColor  : Yellow
    WarningBackgroundColor  : Black
    DebugForegroundColor    : Yellow
    DebugBackgroundColor    : Black
    VerboseForegroundColor  : Yellow
    VerboseBackgroundColor  : Black
    ProgressForegroundColor : Yellow
    ProgressBackgroundColor : DarkCyan
```

You can reset any of these colors to match your preference using the appropriate command `$host.PrivateData.ErrorForegroundColor = "Red"` with your choice of the following colors: Black, Blue or DarkBlue, Green or DarkGreen, Cyan or DarkCyan, Red or DarkRed, Magenta or DarkMagenta, Yellow or DarkYellow, or White.

These settings are ephemeral - meaning that they will hold for the remainder of your PowerShell session, but once you exit the application, they'll have to be reset. 


