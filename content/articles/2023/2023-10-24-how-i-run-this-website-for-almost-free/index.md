---
title: How I run this Site for Almost Free
date: 2023-10-23T09:45:59Z
authors: 
- "Matthew Lamont"
draft: false
categories:
  - Tech Tips
featuredImage:
tags:
  - Indie Web
  - Web Dev
slug: /how-run-this-website-for-free/
keywords:
  - Free Website
description: Nothing in life is free, but we can get really close to it.
---

Running a website takes time, money, and a willingness to learn new things. There is no getting around that, but there are ways to run a website for almost free in terms of financial cost. Today we are going to explore that and I'll explain how I do it for TechTea.io while we are at it.

## You Still Need a Domain

A core reason for having a personal website is to have control over the things you create online. To do so you need to own your URLs. This is where most of your expenses will come from unless you start getting crazy amounts of traffic and if you are getting that much traffic you will not likely be worrying about the cost of hosting.

I get my domain from my old hosting provider Dreamhost, but you can get a domain for much cheaper from places like name [namecheap](https://www.namecheap.com). As long as you go with a common Top Level Domain (TLD) name like .com, .net, etc you will be paying less than $20/year. If the domain you wanted is not available you could try buying it from the owner, but it is often better to just pick a different TLD.

Once you have your domain name set we need hosting.

## Free and Almost Free Hosting

TechTea.io uses [Netlify](https://www.netlify.com) for hosting. It costs me the large sum of $0.00 USD to host the website. 

Why is it free? Well this website is static HTML, CSS, and JavaScript. There is no backend programming language and thus it uses very little resources. As long as I use less than 100GB/month in bandwith hosting is free. 

Netlify becomes much worse of a deal when you go above the free tier for personal websites, but they also provide many features that enterprises use. This is how a lot of platforms get new customers even when providing free services. If a developer has a personal website on Netlify they are more likely to promote the enterprise edition to their company or clients.

As an alternative you can also use [Neocities](neocities.org) to host your website for free. Technically you will not own the domain there as it uses a subdomain like myname.neocities.org, but to get around that you can either pay them for hosting to support the project or you can redirect your myname.tld to your neocities subdomain. This way when someone goes to myname.tld/blog they get redirected to myname.neocities.org/blog. Then in the future when you can afford hosting you can stop redirecting and still have full control of your domain name/content.

## Git Hosting

After creating a Netlify account you will also need to link it to a Github or Gitlab repository. While you should use git for your code projects anyway the main reason we want git is because it integrates into Netlify.

Netlify can take either source code for a static site generator (more on that in a minute) or the static website files themselves from a git repository and host the complete website for you. If you use a static site generator Netlify works as a CI tool that builds and deploys your website from the source files automatically.

You will need to create a github/gitlab account, then make a repository for your website, and finally link it to your Netlify account. I will not go through the steps here as there are instructions when you try to setup a Netlify account.

If you are on Windows you will need to also install git on your computer either from their [website](https://git-scm.com) or Chocolatey. Most Linux distros have git installed already, but if not you can get it from your distro's repos.

I personally use github as it has many tools that make it easy to work with for this use case as much as I don't care for them.

## Static Site Generator

The magic sauce that makes this site possible to run for almost free is a static site generator. A static site generator takes templates, text files, and configuration files and spits out a complete website. There are many different ones out there, but I use [Hugo](https://gohugo.io) as it is fast, flexible, and I was able to wrap my head around it rather easily. If you would like to learn how to use it you can just follow the [quick start](https://gohugo.io/getting-started/quick-start/) guide. 

Basically you either pick a theme or make your own using standard HTML mixed in with go templates. These pages become templates that Hugo will use to generate pages. Then you write your content in markdown. This makes it easy to store everything as text files in git, makes for very small and fast webpages, and makes it easy to rapidly prototype changes you want to make to the website.

## Putting it All Together

Once you followed the steps to build your first Hugo website, you will then need to push it to Github or Gitlab. From there you will need to follow the steps from Netlify to connect your git provider to their service. If you followed everything correctly you will have a website that is mostly free and completely under your control.

If you use Neocities they have a cli tool or you can directly upload the public directory from hugo to their website using their UI.

Once the DNS records from your domain name provider are pointing to Netlify you will be able to see your website at your domain name.

## Going Further

It is really easy to get a website online with these simple tools and thanks to that we can make the web a better place. Consider Open Sourcing your website and placing your content under the creative commons so others can benefit from your creations. Also consider adding [IndieWeb](https://indieweb.org) features to your website. Most Hugo themes don't already have them so it is a great way to familiarize yourself with web development and Hugo as well as join a greater community.

Also if you own a domain name you can create subdomains that point to other servers, this opens up a world of possibilities for self-hosting (maybe a future article) and other fun web projects.