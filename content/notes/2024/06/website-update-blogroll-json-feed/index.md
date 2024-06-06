---
title: "Website Update: Adding Blogroll and JSON Feeds"
date: 2024-06-06T10:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
tags: 
- Website Updates
slug: 
keywords:
- blogroll
- JSON Feed
description: I've added JSON Feeds and a blogroll to my website. Here is how.
---

This website has been a major hobby for me lately. This time I added a couple new features that add a lot to the site. These are a blogroll and JSON Feeds.

## Blogroll

A blogroll is a list of blogs or other sites one reads. In our era of algorithms and AI spam, human curation is more important than ever so I've started several things on this site to help my readers find other interesting things. We have my [Monthly Favorites](/tags/monthly-favorites/) series I started back in January, my new [bookmarks](/bookmarks) section, and now we have the [blogroll](/blogroll/).

This is my first experiment using Hugo's data processing feature. I'm generating the HTML using a YAML file contain data instead of making a static page with markdown like my other posts. This makes it easy to add new blogs and in the future other websites in a structured way. I do plan to clean it up and add features in the future, but here is the basics.

I put my data files in ```/data/blogroll/blogs.yml```. In this file I list each blog like this:

``` YAML
- Name: Manuel Moreale
  Description: Manuel blogs a lot about blogging, the personal web, and random moments in his life. He is one of the first blogs I found when discovering the IndieWeb.
  Website: https://manuelmoreale.com 
  RSS: https://manuelmoreale.com/feed/rss
```
I might add new fields in the future for creators who have podcasts and YouTube channels or major projects, but for now I think this works. A name, description, website, and RSS link are a great start.

Then I created a new layout file in ```/layouts/blogroll/blogroll.html``` with this section below: 

``` Go
{{ range sort .Site.Data.blogroll.blogs "Name" }}
    <li>
        {{ .Name }} <a href="{{ .Website }}"><span hidden="true">Website</span>{{ partial "svg.html" "globe" }}</a> <a href="{{ .RSS }}"><span hidden="true">RSS</span>{{ partial "svg.html" "rss" }}</a>
        <p>{{ .Description}}</p>
    </li>
{{ end }}
```

In my template I loop through my data, sort by name, and print out the values. I have a custom partial I made to display SVG icons and have text that is hidden containing the text of the image as I haven't figured out how to do alt text yet and it seems to work alright in text only web browsers like Lynx. If anyone has a better way to do it let me know.

As for why I didn't just export my RSS Feed and parse the OPML, I tried that. My RSS feed is a bit of a mess and I'd like to do better curation than that. Also YAML feels more human readable. 

I want to use this method for logging books, games, and other media I consume in the future. I'll have a YAML file with the details and then create a page that will display them. If I ever write a review or long comment about them it will link to the article in question.

## JSON Feed

[JSON feeds](https://www.jsonfeed.org) are similar to RSS feeds, but defined in JSON instead of XML. They provide a list of content on a website just like RSS. I already have an RSS feed so why would I add JSON feeds?

Well on one end it is future proofing, it is a new standard that is catching on in the IndieWeb. On the other, there are some cool services I want to tinker with that work better with JSON feeds than they do with RSS. 

JSON feeds are also more customizable than RSS, but I've not tinkered too much with it. 

I followed Gina Häußge's [tutorial](https://foosel.net/til/how-to-add-json-feed-support-to-hugo/) on doing it as I couldn't get the Hugo template I made from scratch working. Gina's worked perfectly so I will not repeat the steps here. You can also just take the templates from this website's git repo if you want to take the code or try it yourself by following Gina's tutorial.

## EchoFeed

One of the reasons for me to setup a JSON Feed was so I could try out [Robb Knight](https://rknight.me)'s [EchoFeed](https://echofeed.app) service. It is a nifty tool that takes your feeds and crosspost (echo) the content to other services like social media.

It is no secret that I don't like social media. It is generally not healthy, is incompatible with nuance, silos your content to places outside your control, and generally doesn't appeal to me even without those issues. I've always been a lurker in online places that are far better at actually promoting community and socializing, I am definitely not going to engage on a platform that is not sustainable and discourages actual deep communication.

All that said, there is value in getting my blog posted further out there on the internet. I don't make money off this site nor do I produce the best and most meaningful stuff, but I want to share my passions and ideas with people and this will help.

On that note, I've made a Bluesky account and will be restarting my Fediverse server in the near future. I won't link to them here yet, but if I find I don't hate them completely I'll start promoting my social links again.

## Other Small Updates

I've added a shameless plug to the footer of posts asking for donations to my [Ko-Fi](https://ko-fi.com/techtea). I already offer all the stuff I create for free so I don't really have much to offer in exchange for your patronage, byt I have it setup as a kind of tip jar. If you find something of value here and want to support me head over there.

I also started tinkering with a small shell script that goes through a directory and optimizes my images for sharing on this site, but it isn't really great and needs some work before I consider sharing it. All it does is run ImageMagick to resize everything to a width of 1200px (the default that my old WordPress theme used) if they are larger and convert the images to lossy JPEG and WebP. I have cut back on using images on the site a lot since converting it over to Hugo, but when I do share images I want them to be as light weight as possible. My website isn't the best out there, but I'd like to think I can at least make my pages lighter weight than most major websites.

As with all things on this site, I'm not an expert so any tips or commentary on any of these new features will be greatly appreciated. 
