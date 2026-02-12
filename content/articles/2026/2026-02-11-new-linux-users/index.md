---
title: "New Linux User Tips"
date: 2026-02-11T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Linux
  - FOSS
  - Philosophy
  - Tech Tips
slug: /new-linux-users/
keywords:
  - Linux
description: With a lot of New Linux users out there comes a lot of questions and missinformation. Here are my tips to keep you from going crazy trying out Linux.
---

A lot of people are jumping on the Linux bandwagon after being abused for too long by big tech companies, but a lot bounce off due to friction and an unwillingness to learn a new way to work. I've used Linux full-time for my personal computing for more than 10 years and used it off and on even before that. That is not to say I'm an expert, but I have an idea of what it is like to use Linux as a daily driver and am definitely more qualified to talk about it compared to a lot of the social media personalities who act like they just discovered it. With that in mind, here are some tips from a casual Linux user so you don't bash your head against a wall trying Linux.

## 1. Be Willing to Learn

Learning is hard, especially when you are used to instant gratification from mobile apps or being bossed around by Windows and Mac. Linux (and UNIX systems in general) is different from most of the systems you are used to. You are going to need to learn new ways of working.

The big thing is reading the documentation, asking decent and good questions, and knowing how to do basic research. 90% of any question you have will be answered on the [Arch Wiki](https://wiki.archlinux.org/title/Main_page) or on your distro's forums/docs. Simple things like using a web browser or installing Steam should require just knowing how your system's package manager works (something you absolutely need to know and have no excuse for not knowing). User management, firewall rules, and the more complex stuff will definitely require some research, but honestly it is usually simpler than it is on Windows (and I know as I have to work with Windows devices for work). A quick search with your favorite search engine will likely net you some answers if you know how to use a search engine, i.e. use search modifiers ([DuckDuckGo Search Syntax](https://duckduckgo.com/duckduckgo-help-pages/results/syntax)). 

Take your time, take notes, and don't worry about getting things correct every time. Linux won't just break because you did something wrong, at least not as catastrophically as Windows does when it can't auth with Microsoft servers.

## 2. For All that is Holy, Don't use Arch, Debian, or Ubuntu Unless you Know What You are Doing!!!

If you are comfortable reading more documentation than most people, are fairly comfortable with tech, and don't care if your computer becomes a project you can ignore this part.

One thing that upsets me about the new Linux hype is people recommending Arch based distros like CachyOS, Manjaro, etc. to new and less tech literate users. There is nothing wrong with these Linux distros, but they are not for people who just want their computer to work. They are for people who are willing to tinker to get their system to work exactly how they want it to work with fairly new software packages. You can learn a lot from using them or better, Arch itself, and it isn't like they are complicated, but they require you to be willing to read documentation, tinker around, and fix things when things break.

Ubuntu was a great distro for beginners back in the day, but I don't think that is the case anymore. They ship defaults that require you to know what you are doing otherwise things might not work as expected (Snaps and a way too small default boot partition in some cases for example). It is a great distro for servers and people who want a reliable system after stripping out the corporate cruft, but I don't think it will serve you well if you just want your computer to work.

Debian is great; it is stable, well documented, and generally just works. It is also FOSS only by default and slow to release feature updates. Neither of these are a problem if you know what you are doing. They are a problem if you want the newest updates to programs, have very new hardware, or are using hardware that needs proprietary drivers to run (Nvidia). 

## 3. Use [Linux Mint](https://www.linuxmint.com) or Something Like It

While distro doesn't matter as much once you have some general understanding of Linux, it does when you start. Your distro determines the desktop environment (the GUI) you will use at first, the programs you will start with and have easily available in a package repository, and the philosophy of how the system works. Don't get me wrong, you can change almost anything about the system you are running to behave like another distro if you want, but if you are just starting out you need sane defaults. [Linux Mint](https://www.linuxmint.com) provides sane defaults.

Linux Mint by default gives you a desktop environment that is similar to Windows, but still more customizable and uniquely its own thing. Uses Ubuntu as a base so all the old info about Ubuntu is relevant, but they removed the corporate weirdness. It is a community run project managed by passionate volunteers. Most importantly, it has a philosophy built around making Linux easy to get into without making the experience like Windows or Mac. 

If you are alright with a little more of a challenge I'd say go with a [Fedora](https://fedoraproject.org) Edition with the desktop environment you want. It has some of the challenges of other ones in my do not use list, but they are usually easier to mitigate and not nearly as bad. A little more willingness to work with it is required though. It has some Redhat corporate nonsense, they are FOSS only by default, and they are early adopters of new tech, but none of it has ever made it too difficult for most people to just pick up and use in comparison to people using Arch or Ubuntu.

## 4. Don't Choose a Distro based on the User Interface / Desktop Environment

I know the screenshots from Garuda Linux speak to the geeky gamer hearts out there, but it is not the distro for most people. The good news is, it is easy to make Linux Mint look like RGB vomit (I say that affectionately and actually like the Garuda default color scheme) or really like anything else for that matter. My little brother is currently using Linux Mint with the KDE Plasma desktop environment, it took him less than a minute to switch to it from the default Cinnamon desktop. He can make his computer look just like my NixOS one without ever switching distros. 

If you want to try another desktop environment or window manager you can either test them in a VM or install it over your current install. It will not only keep you on a stable distro for you to learn on, it will give you a chance to learn more about it. Not saying that trying out other distros is bad, but if you are just starting out you don't want to install a distro that requires you to pick a kernel or manage 3rd party repositories that may break just to test out something that looks pretty.

I do say this with the caveat that you will end up with some duplicate programs and conflicting ways of doing things if you don't uninstall the other environment. I still think it is better for a beginner to use Linux Mint or a Fedora Edition with the desktop you want than trying out an Arch based Linux distro.

## 5. Don't Dual Boot

This will upset some people and is definitely a privileged thing to say, but don't dual boot Windows and Linux. You should install Linux on its own dedicated hard drive, preferably have it be the only thing on the machine you install it on. If you dual boot you will have headaches and will need to troubleshoot. Windows likes to take over things every once in a while with updates being unpredictable and Linux doesn't always play nice with the data on Windows partitions if you try to access it from your Linux partition. It is doable and I've dual booted in my early days, but dual booting got a lot worse with Windows 10 and 11 and even back then I was fixing things till I gave up on Windows all together. 

I understand that not everyone is ready to quit Windows or Mac cold turkey and that not everyone has more than one computer, but you are asking for pain and suffering if you dual boot. Use a VM instead to test Linux if you aren't ready to commit and are unsure if the your software needs will be met. It will save you a headache. 

## 6. Use Compatible Hardware

Before you install Linux on your computer, make sure Linux works with it. Most desktops will just work as long as they are made within the last 10 years (that is 2016 for those of you who still think it is the early 00s). Laptops are usually okay as well as long as they aren't some strange gaming laptop. That said, look at a hardware compatibility chart and common problems with your particular hardware. Either that or buy a prebuilt system that is designed to work with Linux. You will thank yourself later. 

Normally hardware issues are already fixed within a year of a product's release, but make sure that fix is applied to the version of Linux you are using or that your distro patches in those fixes if they run an older Linux kernel. Some hardware will need 3rd party tools to get the best out of them. Do a little research and you will be happy. 

## 7 Learn New Tools

I know I already mentioned this, but Linux is not Windows or Mac or Android or [Haiku](https://www.haiku-os.org). It is different and not all the programs you are used to will work on it. You might have to find alternatives. If you are a photographer you will have to try out digikam, darktable, and rawtherapee in place of your abusive relationship with Adobe, maybe even learn some ImageMagick. If you do video work you might need to test out Kdenlive or if you need more professional software there is proprietary stuff like DaVinci Resolve. Finance has GnuCash, hledger, and Skrooge. If it is a common field there is likely open source software that is free, powerful, and will do 90% or more of the most common tasks in that field.

The open source tools might not be as polished, but they will almost certainly cost you less money and privacy. If there is a feature missing you absolutely need, consider donating to one of the projects that gets close to doing what you need and ask around to see if it is something that can be added.

There is no shame though in sticking with a proprietary Windows/Mac app if you absolutely cannot get the open source tools to do what you need. They might work through WINE, but ultimately you might need to go back to Windows/Mac to get your work done. There is no shame in that. Don't let the open source guys tell you otherwise.

## 8 Ignore Ideologue and the Drama

Like all cults, Linux has had many schisms and has a few very loud idiots. For the most part ignore it, there will be time to learn about the things that matter. Most of the drama is of bigots being kicked out of communities for breaking rules, people who think the old ways are always better, or someone insisting that the old ways were absolutely dumb and there is nothing to be learned from them.

Don't get me wrong, there are some alt-right adjacent agitators like Landuke and projects like Omarchy (made by someone with Bigoted views). I say avoid them, but at the same time it is not worth your time researching why and getting into the drama unless you are into that thing.  

## Ultimately, Do What you Want

This is just my two cents. I could be wrong or someone else out there has better ideas. I genuinely think the two things that will help you out the most will be keeping an open mind and using Linux Mint. At least don't use Arch based distros that are popular on YouTube.

Linux lets you get close to the system in a way that is understandable once you learn it. Some things are difficult and very different, but you will get it. Once you do you will have a lot more freedom and power over your computer than you could ever imagine. Have fun with it.

Find community and feel free to reach out to me if you have any questions about getting setup with Linux.
