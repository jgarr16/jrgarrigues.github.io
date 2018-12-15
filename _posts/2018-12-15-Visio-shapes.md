---
title: "Overlapping Shapes in Visio 2016"
excerpt: How to work around Visio restrictions and overlay shapes & lines when creating graphics. 
categories: tech
thumbnail: wrench
published: true
---
!["Microsoft Visio logo"](/images/microsoft-visio.png)

Ran into a somewhat bizarre hiccup whilst creating a diagram in Visio that I wanted to use for a PowerPoint presentation (so Office-y). I was trying to modify a pre-existing diagram so that I could tell a story, but doing so involved drawing a connector line (see red arrow below) and placing it on top of the pre-existing .png picture. 

!["adding connector line"](/images/visio_edit.png)

Of course, Visio didn't want me to do that by default, so I looked for a workaround. I discovered that you can do this, even if the application doesn't want you to. First, you have to make sure that the Developer tab is available in Visio (if not, [here's how](https://support.office.com/en-us/article/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45)). Within the Developer tab, select Behavior:

!["Developer tab, Behavior option"](/images/visio-dev-behavior.png)

Then, on the Placement tab of the pop-up window, select `Do not lay out and route around` option from the Placement Behavior drop-down box. 

!["Behavior/Placement drop-down"](/images/visio-behavior-placement.png)

The Placement Behavior drop-down might be grayed out for you. If so, move over a couple tabs to the Behavior tab and check the `Box (2-dimensional)` selection from the Interaction Style option. This will make the Placement Behavior drop-down available back on the Placement tab. 

!["Box (2-dimensional) option"](/images/visio-behavior-interaction.png)

That about does it. Hope this helps... 
