---
authors: 
- "Matthew Lamont"
categories:
- Tech Tips
date: "2014-05-04T20:53:43Z"
tags:
- Cross-Platform
- Customization
- Firefox
- Firefox Tweaks
title: How to Restore the Old Firefox Look to Firefox 29
aliases:
  - /how-to-restore-the-old-firefox-look-to-firefox-29/
slug: /how-to-restore-the-old-firefox-look-to-firefox-29/
---

If you are anything like me, you probably do not like the new look Mozilla created for Firefox 29. Fortunately there is a way to change it back. All that you will need is a simple add-on and a two line CSS edit.

## Classic Theme Restorer
The first step will be to install the [Classic Theme Restorer (Customize Australis)](https://addons.mozilla.org/en-US/firefox/addon/classicthemerestorer/) add-on by Aris. This add-on is still in beta so it may contain bugs and we can expect updates in the future.

Once you install it you should go to the Add-ons Manager and find the add-on. Under its preferences menu you are given many options. Some of the basic options I recommend selecting are: Star-button in urlbar, movable status-bar panel, combine stop reload buttons, and Hide add-on bars close button. There are many more options available and I recommend that you try them all out.

The next thing to do is move your icons where you want them. Once you have customized everything to your liking you can right click the customization button and remove it from the screen.

## CSS
Something that you may have noticed was that the Classic Theme Restorer does not give you the option to edit the height of tabs, only the width. The size of the tabs in Firefox 29 are a bit large for small screens, especially if you use toolbars. To fix this we will use a little CSS.

The first thing we want to do is find our Profile folder. The location of the profile folder depends on your Operating System. You can read [this page](http://kb.mozillazine.org/Profile_folder_-_Firefox) to find out where it is on your OS.

Mine is located at: /home/mlamont/.mozilla/firefox/o5meaoc7.default/

Once you find your profile folder we need to make a new folder named _chrome_. Within that folder we are going to make a new text document and name it _userChrome.css_. If you are using Linux, remember that Linux is case-sensitive. Now open the new file with the text editor of you choice. We are going to type the following:

{{< highlight css >}}
@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul");
#TabsToolbar { height: 15px !important; }
{{< /highlight >}}

You may change "15px" to anything you want, but it is a good size.

Now we are done. If you know basic CSS you may want to do some more tinkering with the .CSS file.