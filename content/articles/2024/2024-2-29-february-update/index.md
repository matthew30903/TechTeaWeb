---
title: "2024 February Update"
date: 2024-02-29T08:45:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Website Updates
  - Monthly Review
slug: /february-update
keywords:
  - Update
description: February has been a slow month on this website, but I haven't been completely idle.
---

February has been a slow month on this website, but I haven't been completely idle. Lets take a look at some highlights.

## Website Updates

I've made progress on creating a new review template that makes it easy to write future reviews. I cleaned up the metadata for the reviews I've done so far and created a template to help me stay consistent for future tea reviews.

The new template lets me declare tea properties like recommended brewing temperature, brand, and type of tea all in the front matter of each post. Before I was writing all that info into the body of the review, making it hard to stay constant.

Along with this new template comes some new taxonomy changes.

The taxonomy terms template I originally used had hard coded types, meaning I had to create a new template whenever I created a new taxonomy. Now the template is agnostic and detects the taxonomy from the name of the page it is generating. This means the same template can be used for tags, authors, tea types, and anything else I decide to create in the future. You can find it on the website's [GitHub page](https://github.com/matthew30903/TechTeaWeb/blob/master/layouts/_default/terms.html) if you want a copy of it for your own Hugo site.

As I stated above, there is a new tea taxonomy that lets you sort my reviews by the [type of tea](https://techtea.io/teas/). Unfortunately Hugo doesn't let you easily create sub taxonomies so teas might be classified as both green and gyokuro even though gyokuro is a subtype of green tea. I will probably not ever fix that, but that is okay. I also added [brands](https://techtea.io/brands/), this will be used for both tea and everything else I review in the future.

You can always check out the github and take any of my templates if you find them useful.

## Projects

I have other projects besides this blog that I've been working on:

### RPG Maker

I've been playing around with RPG Maker MZ again. It is not open source, but the code for the engine itself is source available and it is honestly decent software. It is the engine I know best and it is fun to play around with.

I plan to create a little tech demo of the game I'm working on sometime in the future.

RPG Maker is a fun tool to play around with, is accessible enough for anyone to start learning game design, and is powerful enough to do most things someone would want to with a 2D game engine. It is intentionally limited, but thanks to its open nature and the fact it uses JavaScript for plugins it is easy enough to do small edits here and there as needed.

The actual game is a sandbox RPG focusing on economy simulation, base building, and strategic turn-based combat. It is unlikely this will ever amount to anything serious or good per se, but it is a lot of fun to tinker with game development and design.

### Analogue Journaling

I've spoken in the past about using [digital tools to organize my life](https://techtea.io/articles/2023/open-source-productivity-tools-organize-your-life/). I still use all of them except for Logseq. The reasons? Ideas rarely happen when I am at a computer and I love the feel of a good pen on good paper.

There is also some evidence that writing by hand [helps with retention](https://www.scientificamerican.com/article/why-writing-by-hand-is-better-for-memory-and-learning/) and idea generation, but my main reasons are the ones above.

There is a tactility when writing by hand that is impossible to get with a keyboard or even those tablets that come with a stylus. I like the feeling of the nib inscribing the ink onto the paper, the intentionality of cleaning and filling my pen, and the feeling of something taggable when I'm done writing. 

To that end I've been testing out several methods of keeping my notes organized till I can figure out a way of digitizing them that isn't a pain.

I have 3 notebooks, a personal journal that I've been keeping for years but have been fairly inconsistent with, a commonplace book/zettelkasten for keeping long term notes and information, and a small notepad to keep with me everywhere I go so I can capture fleeting notes.

#### Journal

For my personal journal I am going to do a monthly spread that has a spot for each day of the month for a one line highlight note and a habit tracker. When I want to do some more traditional long form journaling I will just date the page like normal and put it after the monthly spread page. This way I have to open my notebook every day and mark something even if I don't write long form.

#### Commonplace Book

The commonplace book is going to be the hard one. It is going to be the entry point into my zettelkasten notes. I don't think I'm going to stick to the idea of a commonplace book as a collection of factual knowledge and quotes and will most likely throw in my own ideas and summarizations. Maybe calling it a commonplace book would be wrong, it is more of a self-reference book.

I've started to take book notes in it and will eventually figure out how to index it. I'm thinking of using John Locke’s Method for indexing first as it seems to be fairly robust.

Once I capture everything if I still feel I would benefit from digital tools I'll digitize the notes here into Logseq and use it as the final zettlekasten.

#### Fleeting Notes

For fleeting notes, initial capture of ideas and information, and short-term todo items that I don't want to enter into Nextcloud I grabbed a small notepad that should be small enough to carry with me everywhere, sit flat on my desk while I'm working, and still be high quality enough to stand up to fountain pen ink.

The initial capture has always been my issue when it comes to taking notes on the fly. Notebooks are always a little too clunky and for some reason a notepad never occurred to me as a possible solution. I know it sounds dumb, but I really didn't think they would be a solution for the problem. Well, my first notepad is coming in the mail and we will see if it works out.

In any case, this will be the notebook for capturing info, then I'll transfer important stuff into the commonplace book after refining it or turn it into an actionable item for the future.

### Helping a Friend with their Website

A friend wanted help creating a website. I won't share too much, but it was very rewarding to help them out and I learned some thing about Hugo along the way. Helping them is what gave me the ideas and motivation for implementing this months website updates.

### 3D Printing

I cannot create very appealing 3D models, but a 3D printer is one of the most useful tools I've ever owned. This month I broke a part of my keyboard's tenting kit. I was able to slap something quick together in FreeCAD and was able to get up and running in a few minutes. It is not very impressive, but I don't have any CAD skills and haven't really spent time with FreeCAD to create anything impressive. If people are interested I might cover 3d printing in the future.

## Other Things

Work takes up most of my time during the week and sometimes it is draining. When that happens I often get in a loop where I end up reading articles or watching YouTube videos. This month I compiled a list of highlights just like I did [last month](https://techtea.io/articles/2024/jan-favs/). I'll publish it soon. Maybe you will find something fun in there.

I also spent the month customizing my Linux install on my workstation. I've been slowly installing packages and applying themes to software installed on my desktop. Default KDE is nice and all, but there are so many themes and styles to play around with. I've settled on the excellent [Catppuccin Mocha](https://github.com/catppuccin/catppuccin) theme, like everyone else was for a while. Maybe I'll apply the theme to this website as well, though I am a little worried about it being too low contrast.
