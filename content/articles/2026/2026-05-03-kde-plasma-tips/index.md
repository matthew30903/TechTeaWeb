---
title: "KDE Plasma Tips and Tricks"
date: 2026-05-03T08:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - KDE
  - Linux
  - FOSS
  - Tech Tips
  - Open Source
slug: /kde-plasma-tips/
keywords:
  - KDE Plama
description: KDE Plasma is has grown in popularity, but it is complex and the advanced features can fall under under the radar. Today we will go over some things I've learned about the desktop environment over the years. 
---

KDE Plasma is very popular right now[^1] and many new Linux users are using it by default. This is wonderful news, but KDE is very customizable, powerful, and has many small features that are underappreciated or outright unknown to most people. I'm by no means an expert, but I've used KDE since the later part of the KDE 4 era and still use the desktop environment as my daily driver.   

Before we start, I'm assuming you already know how to use a computer to some basic competency and already got familiar with the general flow of using KDE's default user interface. I'm also not going to go through KDE and QT based applications outside what would typically be included in a standard Plasma install. I am currently using Plasma 6.6.4 on NixOS so you may have a slightly different experience depending on what version of KDE you are currently on.

Without further delay, here are some cool things you can do with KDE Plasma.

## Tags

You can tag files in Dolphin (Plasma's default file manager) and use these tags to sort your files. 

To tag a file all you need to do is right click on the file then go to **Assign Tags -> Edit tags...** and then either select an existing tag or create a new one. 

There are several ways to access these tags. 

1. Using Dolphin's search feature.
   Click the **Magnify Glass icon in Dolphin's toolbar -> Filter -> Tags** and then select the tags you wish to search for. This only works for top level tags currently (no subtags) and searches all subdirectories. 
2. You can find your tags Dolphin's lefthand sidebar. Click **All tags** or on one of your pined tags to see either a list of all your tags or the files under your pinned tags. These tags work similarly to other directories in Dolphin so you can open them up without going inside of them to see multiple tags at a time or go into one and see a folder with all your tagged files.
3. Query them using KRunner. Open KRunner and then type **tags: <tag you want to search>** and it will list everything. So if you want to find all your cat photos you can just type **tags: cat**. Then select the file you want to open. This also works inside the Applications menu ("Start Menu" for you Windows users)
4. Using the `baloosearch6` command in the terminal. You can use KDE's powerful search features from the terminal by simply typing `baloosearch6 <querry>` so to find our cat pictures we would just type `baloosearch6 "tag:cat"`. This lets you very easily use KDE tags in your scripts.

A couple of things to note about tags: 

1. They are stored in a files extended attributes. This means that you will need to be mindful of them when copying the files as some copying tools do not copy these attributes.
2. They are not standardized. While most KDE applications use these tags, not all Linux programs do. If you are tagging your photos for example, you may want to copy the KDE tags over to the file's metadata before publishing. It also means other desktop environments might not work with the tags so don't invest too heavily into the tags feature if you don't plan to stick with KDE Plasma or other software that supports them.

Alongside tags, KDE Plasma also has a rating feature that works in a similar way. I would highly recommend you look into them if you like to give your files ratings alongside tags.

## Activities

Activities are a bit confusing, but they let you have separate Plasma setups that you can then switch between with keyboard shortcuts or a widget on your panel/desktop. 

This lets you say have a Work mode and a Personal mode on one system. Your work activity could have limited access to games and distracting programs, use a color scheme meant to improve focus, and have all your work programs pinned to the Task Manager. When you are done for the day you switch to your Personal Activity and now all your work applications are hidden, your web browser automatically opens in your personal profile, and your favorite game is pinned to the task bar. 

To create an Activity you can go to **System Settings -> Apps and Windows -> Activities -> Create New...**. Give it an icon, name, and option description. You can also keep the system from turning off the screen or shutting down automatically and prevent it from tracking your files and app usage. If you are going to use the activity a lot I'd also recommend giving it a dedicated shortcut.

This is different from Virtual Desktops as they don't just let you have programs on different virtual 'screens', they are complete desktop setups with their own settings and rules.

Another thing you can do with Activities is use them to test new Layouts or themes for your desktop without breaking your current one. KDE is very customizable so you can very easily change things to look however you want, but it can be hard to revert changes. Activities will let you test different ones. 

Activities are a very powerful feature that doesn't get enough love so check them out and see if they work for you.

## KRunner

I mentioned it in the tags section, but KDE has a built-in application and task launcher named KRunner. It can do a lot, but I mostly use it for opening programs and frequently used files. 

You can open it with ALT+SPACE on your keyboard by default. I'd recommend you click the settings icon next to the search box to edit the settings to your liking. I really like it in the center of the screen instead of the top for example. Also click on the **Configure Search Plugins** button to see all the things KRunner can do. It is a lot.

As I said before, at its most basic it is an application launcher, but you can switch activities, search your Bookmarks, get the definition to words, do basic calculations, convert RGB colors to hex, and a lot more.

I understand people liking things like Rofi and Dmenu, but sometimes we just want something that works out of the box and KRunner does that. One downside of KRunner compared to something like Rofi is that the plugins have to be written in C++, but you [can still write them yourself if you wish](https://develop.kde.org/docs/plasma/krunner/). If you have advanced use cases that KRunner doesn't support you might be better off with Rofi and you can always disable KRunner in the settings, but 90% of people reading this will be happy with KRunner.

## Clipboard Superpowers

KDE's clipboard is among the most powerful across desktop environments. It can store files, generate QR codes, and more. Most are self-explanatory, but here are a few cool ones you might not know.

### Open Clipboard History with Meta + V

You can always go to your clipboard manager in the system tray, but that requires the mouse and distracts from whatever you are doing. Use **Meta + V** to open a clipboard box in the middle of the screen. You can then use the arrow keys or start typing in what you want to find from your history and move it to your clipboard.

### Clipboard Actions

If you open up your clipboard settings by going to the clipboard icon in the system tray, you can configure **Actions**.

Actions give you a way to run commands on your clipboard contents when a pattern is matched. These patterns are going to be regular expressions so you may need to read up on that, but once you do you will be running in no time.

These actions can be configured to show up in a popup window that opens automatically when you copy the text or only show up when you manually click (or navigate using the keyboard) the actions button in the clipboard manager.

This can be very useful for things like opening YouTube videos in MPV or converting photos from the clipboard into other formats.

### Disable/Enable Primary Paste (Middle-click Paste)

This is not a KDE specific tip, but one that effects all of Linux environments except GNOME[^2] desktops. If you middle-click with your mouse, it will paste the last selected text, even if you didn't explicitly copy the text. This is called Primary Paste and might be a little confusing if you aren't familiar with Linux. As an oversimplification, there are two clipboards: The one KDE provides (the regular system clipboard) and then there is Primary Paste.

This feature can be very useful when you are juggling a lot of different contexts in a mouse driven workflow, but it can be rather confusing for some people. You can disable it by going to **System Settings -> General Behavior** and unchecking the **Middle-click Pastes selected text** feature.

If you are coming from Windows where the clipboard is an afterthought, I'm sorry, welcome to the world where your clipboard is a well-thought-out tool. 

## KDE Connect

KDE Connect lets you sync your Android phone with your Linux desktop. You get media controls, the ability to send text messages, notification syncing, clipboard syncing, file transfers, find my phone, and a lot of other general goodness.

If you are coming from Apple you might be used to some of these features, but Windows users are stuck with half-baked phone support. In any case, Linux has very good Android integration if you use it. Most distros include KDE Connect as part of their default KDE Plasma install, but if you can usually install it from your package manager if you don't. 

With KDE connect and the Online Accounts integration in Plasma, you have a full ecosystem that integrates with your phone and cloud accounts. Highly recommend you set this up.

## KDE Wallet

When you first log into a Plasma Session you might be prompted to enter / create a KDE Wallet password. KDE Wallet is a built-in password and secrets manager for KDE, but it is an optional system that not all distros include.

If your distro includes KDE Wallet or you install it yourself, use your Linux user password for the wallet and go into the settings and make sure it never closes. Do that and you will never have to enter the password ever again. 

I say this because there are many, many, complaints about KDE Wallet online that are caused by overly "secure" defaults that some distros ship with or people not understanding how the application works. On some distros it will prompt you for a password every time you log in or interact with a password prompt. Change the settings and you will be much happier.

Go to System **Settings -> KDE Wallet** and disable every Close Behavior option. 

KDE Wallet is very useful and powerful if you know what you are doing. It can store your browser password for you in a more secure way than the defaults do, save your git credentials for GUI text editors, and [store your secrets for scripts you write](/articles/2025/manage-secrets-kde-wallet/).

Most people just use it to store the stuff that normally gets saved by default in a Linux system like Wi-Fi passwords, but it can be really useful if you want to stick to KDE specific applications/don't want to use a 3rd party password manager.

## Keyboard Shortcuts for Everything

I'm not going to go into specifics, but KDE either has keyboard shortcuts for a feature already or gives you the option to set a new one for that feature. 

Go to **System Settings -> Keyboard -> Shortcuts** and take a look around. Almost every feature has a shortcut you can configure.

Some applications will expose shortcuts as well and if they don't you can still create shortcuts to launch them. For example, you can create a shortcut that opens Firefox in a Private Browsing Window even though you sadly can't configure Firefox's other shortcuts here.

You can also create new shortcuts to run commands so if you have a script you run often, but can't automate, you can set a keyboard shortcut for it. 

You can export and import your shortcuts as well, making moving between systems a little less painful.

## Anything I Missed?

There are a lot of features I've not gone over either because I don't know/forgot about them, didn't think they were particularly useful to a newcomer [^3], or thought they were something a newcomer would have found on their own through exploration. Let me know if there are any features I should include in this list and either I'll update it or write a follow-up article with more advanced tips.

I'll go over KDE applications next time I write about KDE. Kontact, digiKam, and a lot of other useful applications need a highlight. 


[^1]: Default on SteamOS/SteamDeck, Fedora upgraded it to an Edition, etc. Also, GNOME keeps making decisions that make it very hard to recommend for anyone outside a GNOME developer.
[^2]: GNOME might almost be onto something here, but then decided to hide the configuration option to re-enable it behind a long terminal command because GNOME isn't made for the average person.
[^3]: Plasma Vaults and Window/Application rules for example are powerful, but most beginners are not likely to need them. 