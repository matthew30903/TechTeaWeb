---
title: "A Glossary of Web Dev Terms"
date: 2024-03-10T08:45:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Tutorials
  - Web Dev
slug: /web-dev-terms/
keywords:
  - web development
description: It is hard to know what you don't know. It is even harder to know when you don't have the right vocabulary to communicate with those who do know. Today we are going over some basic web vocabulary.
series: Into the IndieWeb 
weight: 1
---

It is hard to know what you don't know, especially when you don't have the words to communicate with the people who do know the thing you wish to learn.

Today I'm going to throw out some terms that I think are useful to know when building a website. Hopefully this will give you a bit of help knowing what you still need to learn and help you communicate with others.

For a general roadmap of learning to create your website I'd recommend looking at Mozilla's [Getting Started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) series. I will be linking to their tutorials at the end of relevant terms in this guide.

These are ordered in terms of relevance to a new website owner rather than alphabetical. Let me know if you think something should be higher on the list or if this list would be more useful using another ordering scheme.

## HTML (HyperText Markup Language)

HTML is one of the essential building blocks of the web as we know it. To break it down, HyperText is a type of text that links to other text. In HTML's case this would be other resources on the internet like other web pages, videos, and images. A Markup Language is a language that informs the general structure and rules of text. It says there is a link here or a heading over there. 

Think of HTML as the Bone Structure of your website. It doesn't look pretty on its own, but it lets you know where the navigation links and paragraphs are on your website.

To get started I'd recommend looking at Mozilla's [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML) tutorial. It will give you the basics of how to use it.

## CSS (Cascading Style Sheet)

While HTML is the bones of your website, CSS is the skin. A style sheet is a list of style rules that tell a web browser how to display HTML. It says that the heading should be in a *12pt Times New Roman* font and the color red.

CSS Cascades so you define rules for your styles and they are applied from Top to Bottom, Parent to Child, and from less specific to more specific. So you can create a general rule for all your buttons on your website, then a rule for all buttons inside of a product description, and then a specific rule for only the button named "Buy Now" that is inside the product description. The rules are inherited in the that order with the most specific one, the "Buy Now" button's rules overwriting any conflicting ones from the previous two.

CSS can be a bit confusing when you start getting into more complex setups so I'll avoid going into more details now.

To get started I'd recommend looking at Mozilla's [CSS first steps overview](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps).

## JavaScript

JavaScript is the brains of your website. It is the client side (more on that term in a moment) scripting language of the web. With it you can dynamically change the way your website looks, create complex logic, and otherwise create interactive experiences for your users.

While I'm a firm believer JavaScript should be optional (You can use this website with it disabled), it can also make the web a better place when used properly. It is how the theme switcher works on this website by the way.

Again, Mozilla has a tutorial on JavaScript to get you started in their [JavaScript — Dynamic client-side scripting](https://developer.mozilla.org/en-US/docs/Learn/JavaScript) guide.

## Text Editor

A text editor is exactly what it sounds like, a program that lets you edit text files.

In programming we have two types of files:

- Text: a file that can be opened in a editor and is human readable. This is your HTML, CSS, JavaScript, Markdown, and pretty much everything else you can edit with notepad.
- Binary (BLOB): these are files that are not human readable. These include closed source programs, images, and zip files.

Text Editors often have fancy features that make development easier like syntax highlighting, code suggestions, debuggers, and integration with version control. They often have extensions so you can add features as well.

Kate, VSCodium, nano, emacs, and vim are all examples of text editors. I recommend you play around with them and see what you like. I use VSCodium for managing this website and use Kate for simple tasks.

## Client-side (Front End)

The above languages are what we would call the client-side or front end of your website. This means all the processing is done by the user's computer/web browser after they download the web page.

Usually this means all the stuff written in HTML, CSS, and JavaScript is limited to the users web browser and all the changes made by user input and JavaScript are specific to that user's web browser.

## Server-side (Back End)

Every website needs to be stored somewhere online, this is where servers come in. A server is basically a computer somewhere on a network (in this case the internet) that serves files to computers (clients) that request it.

These servers sometimes just send HTML, CSS, and JavaScript to user's web browsers when they visit a website, but they can do a lot more than just that. Servers can run more powerful programming languages that can interact with databases, generate custom HTML specific to users, and communicate with other network resources.

When we refer to something being server-side we mean it is not processed on the user's computer, but instead on a server somewhere on the internet.

## API (Application Programming Interface)

At a basic level an API is a way for two programs to communicate with each other. On the web this is usually how the front-end and back end communicate with one another.

For example, we have a button on our website that takes a customer's billing info they just filled out in a form. When the customer presses that button some JavaScript sends some information to our server back end to tell it to store that info in a database using an API. Then our server uses our shipping partner's API to tell them a new order came in and to email the customer a tracking number once the order has been shipped.

API's exist in many desktop applications as well, they let you do things like take output from one application and push it into the input of another.

## Web Host

A web host is a 3rd party that provides a server for your website. They host your site so you don't have to worry about running your own server. Hosts often provide extra features like easy to use management tools, web builders, and even technical support. 

## Managed Services

Often when you pay for basic web hosting you are left on your own for actually managing your website. With Managed services your web host will do most of the technical stuff for you in exchange for a higher bill and less freedom.

This can be very useful if you don't want to learn any of the more complex stuff and don't really care about the details other than it working.

## Content Management System (CMS)

Usually managed services will have you use specific software called a Content Management System (CMS) like WordPress, Shopify, or Drupal. These are basically programs that run in your web browser to make it easy to make a website with little coding. 

They create something we call dynamically generated websites. Instead of coding all the HTML, CSS, and JavaScript from scratch for each page the server generates a page either when a user visits said page or when the developer saves changes in the CMS depending on the software. 

If you want to easily manage a website with less technical knowledge these can be great as most have easy UIs to design your site or you need something complex and want a lot of the code already done so you can focus on implementing the feature you need.

The cons are they are more difficult to modify to do things they weren't designed to do out of the box, there is more security concerns because these sites have a more complex back end, and some will make it hard to migrate to other systems or web hosts. 

Some of these are open source and can be used on any web host while others are exclusive to some providers. Ones that can be installed anywhere are often called self-hostable.

## Self Hosting

Lets say you have a home server or an old computer laying around to repurpose as a server. When you run a server on your own without a web hosting provider we call that self hosting.

This is a bit more technical than using a hosting provider, has many security risks, and gives you ultimate control over the hardware and software.

I recommend that you do not host services and expose them to the internet if you don't know what you are doing. That said, having a server to test and experiment on at home can be a great learning experience.

## Version Control

When you work on any coding project you will need a way to save changes you make to your files. This is where version control comes in.

When you make a change to a file a version control program like git, Subversion, and Mercurial all track every change you make so you can easily roll back changes, find out when a change was made, and often who made it (if you are working as a team).

## Repository

A repository is a storage space for your code and assets. Usually we use the term in context to Version Control and Package Managers when we talk about it in web development.

A repository can be local (on your machine) or remote (on a server somewhere) and can usually sync changes between multiple copies of itself. If you have a remote repository of your code you can easily sync changes between all your devices.

## Git

Git is the most popular version control system and you will hear about it everywhere. In git you designate a directory as a repository and the files in that directory can tracked and managed by git.

In practice you will edit your files, tell git you want to publish a change, give it a description of what change you made, and then sync it to a remote git repository or email list (yes git supports using email for collaboration). 

You will also often be pulling down other people's code onto your computer using git when you want to use it in your own projects so even if you end up using a different version control software for your website you will benefit from learning git.

Free Code Camp has a [tutorial](https://www.freecodecamp.org/news/best-git-tutorial/) that also links to other tutorials for git. It is an essential skill for any developer.

## GitHub, GitLab, Codeberg, etc.

You will likely hear about GitHub, GitLab, and many other such websites. On a basic level they provide free hosting of git repositories. They can be your remote repository that you can use to collaborate with other and sync to all your devices. In the Open Source community these places are sometimes called Software Forges.

A lot of git providers also provide extra tools like bug trackers, feature requests, and security testing.

GitHub is closed source, run by Microsoft, and has committed [mass copyright infringement](https://www.theverge.com/2022/11/8/23446821/microsoft-openai-github-copilot-class-action-lawsuit-ai-copyright-violation-training-data), but it is the most popular system and has the most support for 3rd party integration. It include a lot of features that larger teams and projects could benefit from. There is the issue of them training AI on the code on their website, violating the licenses of many of the projects on there.

GitLab is both an open source git repository and a company that provides GitLab as a hosted project. They offer both free and paid plans with advanced features that are geared more towards complex applications.

Codeberg is a non-profit git host that focuses on open source and open culture projects. They don't have as many advanced features as the other two listed, but they also have no profit motive telling them to harm their users like the others. If you are going to publish your website as open source and don't need the features GitHub or GitLab provide I recommend them.

There are many other services so it does pay to shop around and find what works for you.

You can also host a git server yourself or keep your git repo on your own system, but a remote server is going to be the easiest and it takes full advantage of git's features.

## SEO (Search Engine Optimization)

When looking on YouTube or marketing emails from web hosts you will often see the term SEO. This stands for Search Engine Optimization and basically involves techniques to improve the position your website gets in search algorithms.

This generally involves providing good metadata about your website (titles, type of content, tags, keywords, etc) and writing in a way that search engines like. If your website is meant to sell commercial products this will be something to optimize for. If you are building a personal website I say don't think too hard about it and create good content. SEO is for robots, humans want to read something useful or interesting.

## Static Site Generator (SSG)

Static Site Generators can be seen as the opposite of a CMS. They usually take text files (usually Markdown or txt) you write, templates written in the web languages mentioned at the start of this list and a template language, and combine them into a webpage.

This makes it easy to write a web page once and then focus on your content from that point forward. They output HTML, CSS, and JavaScript with no back end, this usually makes the pages really fast compared to a modern website written with popular frameworks or a CMS. The major cons are that they are complicated for people not familiar with web technologies and as they have no back end there are limitations on what you can do directly on the website. You have to get a little creative when doing things with static websites and that creativity needs some experience.

This website uses the Static Site Generator Hugo, but there are other good ones like Eleventy (11ty) and Jekyll. I would recommend this if you want more freedom and control over your website, but only want to work with frontend technologies.

## Frameworks

A framework is software that helps you create websites by pre-writing a lot of the code for you, often including themes, and having an opinionated workflow so you don't have to worry as much about how to go about doing something.

Unfortunately in the world of web development many of these frameworks are designed for creating applications and not personal websites. This often means they don't work with JavaScript disabled, they are often lack accessibility features by default, and can be slow. This doesn't apply for all frameworks mind you, but I would recommend you avoid them till you already know the fundamentals of web development.

## This list is ever expanding

Please let me know if there is a term I missed that would be useful for a new website owner. Let me know if there are things that shouldn't be here as well.

There is always a blindness when you know something. Something that might be obvious to me might not be to someone who has never coded before.