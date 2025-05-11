---
authors: 
- "Matthew Lamont"
categories:
- Tech Tips
date: "2016-09-06T11:00:22Z"
tags:
- Firefox
- Firefox Tweaks
- FOSS
- Tutorials
title: Customizing Firefox
aliases:
  - /customizing-firefox/
slug: /customizing-firefox/
---

Update 2023-06-30: Removed link to Adblock Plus as Ublock Origin is what I use and has less controversies. Removed Link to Classic Theme Resotorer and Add to Search Bar as the links are dead. Firebug was integrated into Firefox and is no longer available. I also replaced Stylish with [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) as Stylish was purchased by an adware company. VimFX link is also dead and has been replaced with [Vimium-FF](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/) I will keep the text of the article as is however.

The reason we chose [Firefox](https://www.mozilla.org/en-US/firefox/new/) as our web browser in the [Introduction to Computers](https://www.blog.mattlamont.com/internet-introduction-computers/) series is due to its great customization features. By using Extensions and Personas we can make Firefox our own. Make sure that you have the [program installed](https://www.blog.mattlamont.com/internet-introduction-computers/#Installing-Firefox) before continuing.

## Personas: Firefox's Skin

The easiest way to customize Firefox is with a Persona. These are similar to wallpaper on your desktop, but cover the browser toolbars. You can find them on [Mozilla's Firefox addons site under themes](https://addons.mozilla.org/en-US/firefox/themes/). To apply a Persona just click the "+ Add" button. You can also test a theme without installing it by hovering over it with your cursor.

{{< figure src="./img/Firefox_Personas_Ex" alt="Image: Firefox Theme">}}

In the past Firefox had a much more powerful theme system that could change the whole layout of the browser. Due to some unfortunate design decisions they have simplified the system and made it more difficult to achieve system wide changes.

If you would like to know how to make your own persona you can, we will go over how to do so in a future tutorial as it will require some image editing.

## Extensions: Make Firefox Better

Firefox is rather powerful on its own, but some things that should be default are not and some things need to be fixed. This is where extensions come in. These are bits of code that add functionality to the browser. All of the extensions that are peer and Mozilla reviewed, if something is bad it will not stay for long if it ever gets approved in the first place. You should not install addons/extensions from untrusted sources.

We will go over some of the most useful and fun extensions in this article.

### Adblock Plus / [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)</a>

{{< figure src="./img/Adblock_Disable_Ads" alt="Image: Blocked Ads">}}

Most websites make money using ads, without them we could not afford to keep in business. There comes a time, however, when ads are obnoxious or even harmful. Video ads, animated ads, scams, etc. Ads slow down your browsing experience. These two extensions are the most known and respected ad blockers around. Either one will work, but Adblock Plus has had some shady deals with advertisers and has some issues with high CPU usage.

If you chose to install Adblock Plus, disable "Allow some non-intrusive advertising" option in the options.

Also consider adding us to your browser white list by clicking on the extensions button and clicking "disable on this domain"

You can add either one by simply clicking the "+ Add to Firefox" button.

### Classic Theme Restorer

{{< figure src="./img/Firefox_Classic_Theme_Restorer_Options" alt="Image: Classic Theme Restorer Options">}}

I have already gone over this extension [in the past](https://www.blog.mattlamont.com/how-to-restore-the-old-firefox-look-to-firefox-29/). Remember how I said that Firefox use to be more customizable? This plugin gives some of that customization back. You can change the style of tabs, the menus, and more importantly the search box. One of the biggest issues with the design direction in the newer Firefox is the search box functionality. The decision prevents you from quickly switching between search engines in favor for one click searching. In the Classic Theme Restorer options you can set the behavior back to a more useful state.

### Stylish
Keeping with the theme of Customization, Stylish allows you to to theme websites with custom CSS. Basically personas for websites. If you find that a website is too light or has a bad color scheme, you can change it yourself or in most cases find a theme that someone has already made for you. Though it is mostly cosmetic, it is useful to have and will surprise your friends when Google looks different.

### [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/)

Moving away from cosmetics and into functionality, Greasemonkey is the Swiss Army Knife of extensions. It functions similarly to Stylish. By itself, Greasemonkey is useless, but by applying userscripts you can change anything on the web. Userscripts are like mini-extensions written in JavaScript. Some auto-load the next page on Google, while others [change the way Facebook works](http://socialfixer.com/download.html) all together. You will have to work at this one for it to be useful, but useful it is.

### VimFx

VimFx brings Vim-style keyboard shortcuts to Firefox. It is a bit complicated to go over in this article, but keyboard shortcuts make everything faster. With VimFx, pressing "x" will close a tab, "t" will open a new tab, "o" will activate the search bar, and "i" will disable the shortcuts. The extension is not perfect, you cannot exit insert mode when on YouTube as it has its own shortcuts for example, but VimFx provides great shortcuts that will save anyone time.

### Firebug

Firebug allows you to make live changes to a website's source code. This may sound a bit complicated to a normal user, but it is very useful. Some website will have full page ads that block content and do not go away even with ad blockers for example. You can disable the ad by erasing the line in the source code or adding a new CSS rule. It is also useful for web developers and designers when mocking up website changes.

### [Disconnect](https://addons.mozilla.org/en-US/firefox/addon/disconnect/)

Most websites track you. Ads track you, Facebook, Amazon, even my website has some trackers. Sometimes they are harmless, just to keep you logged into your account. Often they are malicious. Amazon and Facebook do not need to know that you are looking into buying a computer and that random Chinese advertising agency does not need to know that you are talking to your grandma on Facebook. To help prevent these issues Disconnect blocks the invisible tracking elements on websites. This will often speed up website load times as an added benefit. Remember, you should never need to sacrifice privacy.

### Add to Search Bar

Have you ever been on a website or custom search engine and wanted to search with it directly from the search bar? Unfortunately very few web browsers have a way to easily customize your search engines. Fortunately this extension gives you the ability to add any search box to your search engine list. If you are a student you can finally add that search database that your school uses to Firefox.

We hope that you have found this article helpful. What web browsers do you use?