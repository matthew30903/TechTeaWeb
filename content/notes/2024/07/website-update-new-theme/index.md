---
title: "Website Update: New Theme"
date: 2024-07-23T10:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
tags: 
- Website Updates
slug: new-theme
keywords:
- theme
description: TechTea has a new theme.
---

[James](https://jamesg.blog/2024/06/28/new-design/), [Matthew Graybosch](https://starbreaker.org/blog/tech/starbreaker-org-holy-grail-layout/index.html), and [Wouter Groeneveld](https://brainbaking.com/post/2024/06/introducing-the-new-brainbaking-theme/) all redesigned their websites recently and it really inspired me to try something I've been meaning to do for a while now. I rebuilt my website's theme almost from scratch.

## The Why

Web development and design are not my strong suit so in the past I've stuck to prebuilt themes. This is great in that it gives me a website fairly quickly and it will usually look good, but the big problem with that is I don't know where everything is to make changes.

This site was using the fantastic [Poison](https://github.com/lukeorth/poison) theme before and it ticked a lot of boxes for me, but it has a lot of features I don't use and it was a little hard to modify things without knowing its internals well.

That lead me to creating a new theme.

With this new theme I should be able to create new features and change things fairly easily. My page size is really tinny now too as it isn't loading a bunch of CSS and JavaScript. The size will undoubtedly grow as I figure out new features and techniques to make the website, but now it will only have the features I need and nothing else.

## The How

Hugo has a command for creating a new theme that was not in the quickstart guide. Fortunately it is [documented](https://gohugo.io/commands/hugo_new_theme/), but I wish it was in the introduction tutorial for people who want to build their own systems.

``` hugo new theme [name] [flags] ```

This creates a new theme with a bunch of working boilerplate. 

I followed this [guide](https://matthewjamestaylor.com/holy-grail-layout) to get the layout. It is a simple 3 column layout with a footer. This idea came from the fact that I always liked sidebars and [Matthew Graybosch](https://starbreaker.org) did the same on his website.

After that I tried to create a dark mode. First I tried using the system default theme following the info from Sara Joy's blog post [Do you know color-scheme?](https://sarajoy.dev/blog/color-scheme/). It worked, but didn't give the desired results so I started tinkering and found Adhuham's [article](https://css-tricks.com/a-complete-guide-to-dark-mode-on-the-web/) on CSS Tricks that gives some awesome code and ideas for creating good dark modes.

I did have to modify the code, but it worked. Then I took the switcher icon that was used by Poison and copied their technique of declaring CSS variables in a template so I could define colors from hugo's config file.

I took my review, bookmark, and about page templates as well as the social icons from the Poison Theme after getting the basics working.

With all that I was able to create this theme.

## Theme Features

The new theme is fairly simple, but I've done a few QOL things that I think will make it easier for me in the future to build out new pages as my needs change and grow. 

- Full Text RSS. I got an email from [Wouter](https://brainbaking.com) reminding me that my RSS feed was still showing summaries. I updated the default template and now everyone should be able to enjoy the articles their preferred way. Let me know if you notice any issues.
- Started organizing templates by type. This is something I missed when reading the Hugo docs, but templates can be sorted into folders like so: type/template.html. This really makes a lot more sense than how I was trying to do it before. Right now only the pending collections page is setup like this, but all old pages will be in the future.
- Light weight. Right now the heaviest page on this site is sitting at a little over 300kB according to my browser's developer tools. Most pages are under 100. This means the website is hopefully more accessible to people with limited bandwidth and older devices. The only JavaScript so far is just for the Dark/Light mode toggle.
- Semantic HTML. A large part of the web is not accessible to people who do not have site and traditional input devices. I've been learning a little more HTML and general web development lately and tried to make this website more accessible. Please let me know if you find any part of this site hard to read, access, or otherwise use.
- A Footer Area. Poison didn't have a footer area, instead having all menu items in the sidebar. I have far more pages now than just the blog itself and don't want to clutter the sidebar with them. This is likely something I'll get working on soon.
- Uses users default font. I don't know if this is something I'm going to keep or not, but the theme should use the font you have setup in your browser rather than some web font. Hope that helps with accessibility.

There are probably small things I'm forgetting, but this should cover the major things I've done with the new theme.

## The Future

I am now working on the future tea database page that will log all the teas I drink, where to get them, how I categorize them, etc. It will be the next major update to the site as long as I don't get distracted. I'm almost ready to publish the prototype.

Please let me know if you notice any bugs or have ideas to make the theme better. The goal is to be easy to extend, modify, and read.
