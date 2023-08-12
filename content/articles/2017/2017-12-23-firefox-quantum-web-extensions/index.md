---
authors: 
- "Matthew Lamont"
categories:
- Philosophy
date: "2017-12-23T09:00:18Z"
tags:
- Computer
- Cross-Platform
- Firefox
- Firefox Addons
- FOSS
- Open Source
title: Firefox Quantum and Web Extensions
aliases:
  - /firefox-quantum-web-extensions/
featuredImage: ./img/ff_Quantum.png
slug: /firefox-quantum-web-extensions/
---

With the introduction of Firefox Quantum, Mozilla removed support for legacy XUL extensions in favor of Web Extensions. This naturally made a lot of people angry. XUL extensions had full control over the browser and could change everything from how downloads where handled to the user interface. This powerful framework gave Firefox what many seen as a competitive edge. Extensions this powerful came with some shortcomings, however, and this lead to the adoption of Web Extensions in Firefox.

## The Problems with XUL Extensions

We already established that XUL is powerful. Many of the most popular extensions, [Classic Theme Restorer](https://www.blog.mattlamont.com/customizing-firefox/) for example, are written in XUL. They are able to change most aspects of the browser, make complex themes, and essentially rewrite parts of the browser. This comes with some inherent risks:

* Extensions are single processor.
* Updates can brake extensions.
* Extensions can break browser functions.
* Extensions are not sandboxed.

XUL Extensions are powerful, but are unstable. If Mozilla wanted to add a new feature or change a function in Firefox, they would risk breaking popular extensions. This held Firefox back and kept Firefox from developing much needed features such as multi-processor support and tab sandboxing. Imagine a tab crashing and your whole browser crashing in the process, not very fun. Powerful extensions that could change every aspect of the browser are not secure, break things, and keep the browser in the past.

Very few extensions actually needed XUL to function and the technology was putting Firefox behind other browsers.

## Web Extensions

Web extensions are written in HTML, CSS, and JavaScript. These extensions are written in the same languages as the web and have some advantages over XUL:

*   Extensions are more secure.
*   Extensions are unlikely to brake.
*   They can run in their own process.
*   Web languages are more accessible to developers than XUL
*   Extensions are cross-platform

Web Extensions cannot change core browser features. This is a mixed blessing. They cannot add a sidebar or give you a debug console for example, but by the same token they are not able to hijack core functions of the browser and are unlikely to change something that will get updated. That said malicious extensions do exist and they could break with an API update. Firefox can now develop much more rapidly without breaking things.

These extensions come with a new Firefox built to handle the modern web. The browser can now handle multiple processes. Tabs no longer bring down the rest of the browser with them and run in their own sandbox. Undoubtedly Quantum is a faster browser. Firefox would have continued to lose its market share without these improvements. How can the "Browser with a mission" complete that mission without users, funding, or developers?

## The Future of Firefox

Web Extensions are likely the future. They may not be nearly as powerful as legacy extensions, but the benefits outweigh the downfalls. Most other web browsers use web extensions, implementing the API allows for cross-platform extensions, greatly expanding Firefox's plugin library. Chrome, Opera, Vivaldi, and others all use the same underlining technology.

Mozilla has not just been copying other browsers. They know that web extensions lack functionality and have enhanced Web Extensions. Extensions in Firefox are far more powerful than in their competitors. The move away from extensions has also prompted the idea of making the browser more powerful out of the box. New ideas and built in features will come with time.

Firefox is one of the few major open source browsers with power to shape the web. Firefox is still one of the most customizable browsers online, even without the power of XUL extensions. The commitment to privacy is commendable, but now Mozilla has something to back up their ideals.

You can find out more about web extensions from [Mozilla's website](https://wiki.mozilla.org/WebExtensions/FAQ) and [learn how to write your own here](https://developer.mozilla.org/en-US/Add-ons/WebExtensions).

## Aside

Will I still be using Firefox? Perhaps in the future, but for now I will be using Vivaldi as Firefox matures. Firefox's sidebar is half-backed; the UI is customizable, but limited; and the built in features do not compare to Vivaldi's. Firefox is a good browser, Mozilla is improving, and they have a future. [Bad marketing decisions](https://www.cnet.com/news/mozilla-investigates-mr-robot-firefox-extension-problem/) and [deals aside](https://blog.mozilla.org/firefox/update-looking-glass-add/), Firefox is an open source browser that respects your privacy.