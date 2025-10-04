---
title: "Maketober Week One 1st to the 4th"
date: 2025-10-04T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - RPG Maker
  - Creativity
slug: /maketober-week-one/
keywords:
  - creative
description: October is going to be the month of creating. Maketober as it were. Here is what I've done so far.
---

I need a distraction from the things going on in the world and have been thinking about making more stuff in general this month. To push for that goal I've decided to do something creative each day this month. No major constraints and it can be as small as snapping a photo, as long as it is deliberate and constructive. Calling it Maketober because I'm not very good at names nor am I actually that creative. The Youtuber [Evan Monsma](https://www.youtube.com/@EvanMonsma/videos) is also making something each day this month, his projects are an inspiration to me and kinda prompted me to try something similar.

With that in mind, I have a website so I thought it a good idea to share my progress.

## Publishing my September Review (Day 1)

First thing I do every month for this website is review all the notes I collected over the prior month and compile them into my [monthly review](/tags/monthly-review/) post. September was a pretty good month all things considered. I tried to highlight some people I've only recently found or that I don't share often. With me doing this create something challenge I feel like there will be more personal stuff on the October review.

## RPG Maker Project (Day 2 to 4)

So I've been doing a lot of stuff related to RPG Maker MZ and will probably do so throughout the month. RPG Maker is not the best game engine out there, it is not native to the OS I'm using, nor is it open source. You could say it is not the right tool for the job, but it is a lot of fun. 

Without going into too much detail, I'm building an RPG with a strong focus on the Magic System, Base/faction Building, and a fantasy world simulation. I had a much wider scope at first, but have narrowed it down to those things. 

Anyway. I got the urge to build a world map and thought to myself "Wouldn't it be cool if I could hover my mouse over a region and have a popup show details about that region?"

The basic requirements were that I needed a way to get the mouse coordinates on the screen, then convert them to tile coordinates (RPG Maker MZ defaults to a 48x48px grid), and then grab the region ID for that tile (RPG Maker has a Region system that is normally used for random encounters). The region ID would then be used to determine text that would show up in a text box on the screen.

I spent hours iterating on the idea; the [RPG Maker script call reference](https://forums.rpgmakerweb.com/index.php?threads/rpg-maker-mv-mz-script-call-list.46456/) and a text editor open on one screen, the engine on another. I did not know what I was doing and it really shows. I tried to do some math that I've not used since high school to find out the tile location of the cursor relative to the player. It never worked.

I asked on the [RPG Maker forums](https://forums.rpgmakerweb.com/index.php?threads/get-map-coordinate-under-cursor.180395/) for help, it turns out there is a built-in function to convert the mouse location to tile coordinates. With Canned_Dinosaur's answer to my question I got something working.

For the Map I use the following code in a parallel process event:

```JavaScript
let tileX = $gameMap.canvasToMapX(TouchInput.x);
let tileY = $gameMap.canvasToMapY(TouchInput.y);

$gameVariables.setValue(10, tileX);
$gameVariables.setValue(11, tileY);
$gameVariables.setValue(12, $gameMap.regionId(tileX, tileY));
```
This captures the touch tile ID of the position the player is hovering the mouse over, stores those in RPG Maker's own variables in case I need them for something else in the future (could be completely removed for this use case), and then captures the region ID of the tile the mouse is hovering over and places it into the RPG Maker variable 12.

I use a few RPG Maker Plugins from the talented team at VisuStella for some of the advanced aspects of the game. Their plugins are very versatile and with a little JavaScript, RPG Maker Eventing, and their plugins you can make some fairly complex systems.

I display a text window using [VisuStella's Visual Text Window](http://www.yanfly.moe/wiki/Visual_Text_Window_VisuStella_MZ) plugin.

I'm also using their [Visual Fogs](http://www.yanfly.moe/wiki/Visual_Fogs_VisuStella_MZ) plugin to highlight each region.

The result is very nice:

{{< figure src="./img/rmmz_map_1" alt="RPG Maker Map with highlight and mouse over tool tip.">}}

All that was yesterday and the day before. I still have the debug data in there and a bunch of small changes to make with how I store the region info, but it is working.

Once this article is posted I'll start brainstorming how to actually present and store information.

## Little Farmer's Market and Date with my Partner (Day 4)

I went with my girlfriend to the Little Tokyo farmers market as part of our normal Saturday date. I took several photos while there, still need to go through them though.

## Should I post an update every week?

I don't think I'll post everything I do, but I was thinking of posting weekly updates on the project. What do you think?

A lot of the stuff I'll be working on is likely going to be RPG Maker related, but I also have some blog post ideas and a few other projects I want to get done this month.

Please share your creative endeavors using the email below this post, I'd love to hear them.

This post is also part of Day 4's creative work.


