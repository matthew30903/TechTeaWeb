---
authors: 
- "Matthew Lamont"
categories:
- Tech Tips

date: "2014-12-02T09:18:07Z"
tags:
- Cross-Platform
- Firefox
- Firefox Tweaks
- Free Software
- Open Source
title: 'Quick Tip: How to Use the Old Search Box in Firefox 34 or Later'
aliases:
  - /quick-tip-use-old-search-box-firefox-34/
slug: /quick-tip-use-old-search-box-firefox-34/
---

Firefox has experienced a major update with built in chat and a new search box. Some of you may find the new search box inconvenient if you use multiple search engines regularly, fortunately there is an easy fix to the problem.

To use the old search box in Firefox in version 34 or higher you will need to edit the configuration settings.

Type about:config in the URL bar to see Firefox's settings. Hit "I agree" If prompted.

There should be a search box on the top of the page type this into the box:

browser.search.showOneOffButtons

Set the setting to false by double clicking it or right clicking and hitting **Toggle**.

After resetting Firefox the search bar should act like it did in earlier versions of Firefox.