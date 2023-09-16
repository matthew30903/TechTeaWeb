---
title: "Website Update: Cleaning the Footers on Posts"
date: 2023-09-16T11:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
categories: Website Updates
tags: 
- Website Updates
slug: website-update
keywords:
description: Added webmentions, fixed the footer, and now you can contact me.
---

A lot has changed in the backend of the website, most of it not visible, but still important work.

The most important thing is I fixed the footer on the website. Before it was getting the last page in a hardcoded section, in Hugo each post type is a section. The theme was using these hardcoded sections so that caused a bit of difficulties. Now it uses ```.PrevInSection``` and ```.NextInSection``` to get the Section of whatever I post, be they [Articles](/articles), [Notes](/notes), [Reviews](/reviews), or whatever I come up with next.

The other big thing you will see is a email link at the bottom of the page right after the author section. This was inspired by Manuel Moreale's post on [Online Conversations](https://manuelmoreale.com/online-conversations) and the footer of every post on his site. I have a general dislike for social media and agree that private conversations are the best way to communicate so feel free to drop an email.

On the back end I've started working on implementing [webmention](https://indieweb.org/Webmention) support on the website. Currently techtea.io gets them, but I am still working on consistently sending them. Webmentions make it easier for websites to communicate with one another and helps create a more open web.

There is probably a lot of small things I'm forgetting, but I'll keep everyone updated as things move forward.