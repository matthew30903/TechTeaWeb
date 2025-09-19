---
title: "App Spotlight: Newsboat, a Terminal RSS Client"
date: 2025-09-18T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - RSS
  - App Spotlight
  - Linux
  - FOSS
  - Open Source
slug: /newsboat/
keywords:
  - Newsboat
description: Newsboat is a terminal RSS reader that makes the internet a better place.  
---

[RSS is awesome technology](/articles/2020/rss-our-information-diet/) that makes the internet fun, but to use it you need an RSS feed reader. There are many options available, but the one I've stuck to the longest has been [Newsboat](https://newsboat.org).

Newsboat is a fairly simple RSS reader that lets you check your feeds from your terminal. There are many GUI and web apps that can do what Newsboat does, but I've yet to find one as customizable and as fast as it. Today we are going to go over the basics of getting it up and running.

## Getting Started with Newsboat

Before we get started you will need to be on a Linux, FreeBSD, or macOS system to use Newsboat. If you are on Windows, bless your heart, you can use the poorly name Windows Subsystem for Linux to run Linux programs on the OS. Also, almost everything I have to say can be found in the [documentation](https://newsboat.org/releases/2.40/docs/newsboat.html) so feel free to read that after you are done here.

You can usually find it in your OS's package repository, but there is an option to build from source that can be found on the Newsboat website.

Once you download the program you can run `newsboat` from your terminal. As you likely don't have any feeds or configuration setup it will not do anything yet.

After running the program for the first time you should see a few new configuration files generate in the `~/.newsboat/` directory.

### Adding Feed URLs

A feed reader is not very useful without feeds. You can import an opml file if you used a prior RSS reader by using the `newsboat -i <feedFile>` or open the `~/.newsboat/urls` file to start adding feeds manually.

The structure of Newsboat's `urls` file is really simple, but gives you quite a bit of power to work with. They follow this simple format: 

`URL "Tag" "Tag" "and even more tags" # Comment`


Here is an example to get you started (All of these are real except the last two, they are examples for doing more advance things):

```
# Personal Blogs
https://techtea.io/index.xml "Personal Blogs"
https://vkc.sh/feed/ "Personal Blogs"
https://manuelmoreale.com/feed/rss "Personal Blogs"
https://brainbaking.com/index.xml "Personal Blogs"

# Projects I Follow
https://openmw.org/en/feed/ "Projects I Follow" # OpenMW

# Tech News
http://feeds.feedburner.com/arstechnica/index "Tech News"
https://planet.kde.org/index.xml "Tech News"

# YouTube - Philosphy
https://www.youtube.com/feeds/videos.xml?channel_id=UCct9aR7HC79Cv2g-9oDOTLw "YouTube - Philosphy" # Religion for Breakfast

# https://username:password@hostname.domain.tld/feed.rss # Replace username and password with the ones for the feed.

# file:///var/log/rss_eventlog.xml # Even files on your system can be feeds in Newsboat
```

You can have any number of tags you want, but the first one is special. The first one can be displayed in your Newsboat UI for better sorting of feeds. As you can see here, I use the tag to sort my feeds by type.

## Navigating Newsboat

Once you have added feeds to your list you can open Newboat again and you will see all your feeds. They may take a moment to load depending on how many you have, but Newsboat does cache them, so future launches should be faster.

Newsboat has three main views that are navigated in this order Feed List View → Article List View → Article View

Feed view shows all your feeds, Article List is all the articles from a particular feed, and Article View is the actual article itself. Not all RSS feeds publish their full articles so you may need to open them in an external viewer. 

By default, you can navigate the list using the arrow keys, use Enter to open an item, and press q to close the item or on the main Feed List view close Newsboat. Use `o` to open articles in your default browser either from the Article List or Article view. `R` reloads all your feeds and `r` reloads the selected one.

## Customization

Newsboat has a lot of features under the hood, but to access them you will need to edit the config file.

This file will be `~/.newsboat/config` and due to the complexity of the many options I'd recommend reading the [documentation](https://newsboat.org/releases/2.40/docs/newsboat.html#_configuration), but I will give an example from my configuration.

```
refresh-on-startup yes # Reloads all the RSS feeds on startup

auto-reload yes # Turns on Auto Reload
reload-time 120 # Sets the Auto Reload to 120 minutes

reload-threads 10 # Uses 10 threads at once when reloading feeds. Lower this if there are issues loading feeds
show-read-feeds no # I don't like empty feeds on my list so I hide them
show-read-articles no # I hite read articles as well
goto-next-feed no # By default newsboat will look at the next feed once you've read the articles in a particular feed when using the next button. I don't want it to do that so I disable it. 

browser vivaldi # Set Vivaldi as my default browser

macro v set browser "mpv '%u'" ; open-in-browser ; set browser vivaldi # Creates a macro that opens a URL in mpv when I press :v. I use this to play YouTube videos without opening YouTube

ignore-article "*" "title =~ \"#shorts\"" # removes articles/videos with #shorts in the title. I hate YouTube shorts

feedlist-format     "%4i %< %25T %10u %t" # This is a custom format for the feed list I think looks good.

feed-sort-order firsttag # I sort my feed based on the first tag, makes it easy to organize my articles.
```

If you read articles on multiple devices you can set up Newsboat to pull and sync with a bunch of online services. I was doing this with Miniflux and NextCould news in the past, but now I just read RSS from my computer.

You can apply themes, customize shortcuts, and run external scripts using Newsboat's configuration. We are just scratching the surface here.

## Why Newsboat?

I've played around with a bunch of RSS readers. There are many with powerful features, beautiful GUIs, and more. Newsboat was the only one that gave me all the features I wanted alongside being able to sync feeds with the software I used on my phone back when I used my phone and computer for reading.

It has a bunch of cool little things like the macro function that lets me remove the annoyance of YouTube while still being able to watch videos and has a nice TUI that gets the job done fast.

The only problem I've ever had with it is that it will occasionally crash if I scroll through my feed too fast while it is refreshing the feeds. That could honestly be fixed by disabling the auto refresh as I don't really need new updates that often.

Thank you for reading.

Have any of you used Newsboat? What do you think? Do any of you have any other software recommendations I should check out or do a spotlight on? Let me know.
