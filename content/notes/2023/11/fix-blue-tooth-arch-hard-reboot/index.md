---
title: "Fixing a Bluetooth issue on Arch Linux"
date: 2023-11-01T11:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
categories: Tech Tips
tags: 
- Tech Tips
slug: fix-bluetooth-arch-linux
keywords:
- Bluetooth on Linux
description: Bluetooth stopped working on my desktop, but it was easy to fix.
---

Every once in a while something breaks when running Linux. In my case my bluetooth randomly stopped working when I updated the kernel version.

Naturally I thought it was an update that caused the issue so I rolled back, but that fixed nothing. Resetting the bluetooth service though returned:

```
groot systemd[1]: Condition check resulted in Bluetooth service being skipped.
```
I decided to wait a few weeks to see if an update would fix the issue, but nothing came around so I decided to check online for help.

I came across this helpful comment on the [Arch Linux forums](https://bbs.archlinux.org/viewtopic.php?pid=1833848#p1833848):

> Another cold boot resolved the issue.  
> -*blackfedora*

An obvious solution, but one that never occurred to me and I work in IT for a living. It happens to the best of us and I'm far from the best.

In any case, to preform a hard/cold reboot:

1. Simply shut down your system.
2. Flip the power switch on your power supply if you are on desktop or remove the battery from your laptop if it is easily removable and you are using a laptop.
3. Hold down the power button on your system for 15-30 seconds. This drains the system of residual power.
4. Plug everything back in and turn it on.

Why did this work? Sometimes hardware gets stuck in a strange state and draining all power can fix it. This solves way more issues than it should and does wonders at my work.

This is not a silver bullet and many other things could have been wrong, but this fixed my issue and I can use my headphones wireless again.

I hope this might be useful to someone out there with the same issue so I thought I'd share it here.
