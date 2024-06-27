---
title: "Quantified Self and Self Data Collection"
date: 2024-06-26T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Indie Web
  - Personal
  - Productivity
slug: /quantified-self
keywords:
  - Data
description: I've always like tracking my personal data. Knowing my sleep patens, what I've eaten, what I've read, my mood from a year ago, etc. It is fun. Here are my thoughts on the subject.
---

I've always like tracking my personal data. Knowing my sleep patens, what I've eaten, what I've read, my mood from a year ago, etc. It is fun. Unfortunately I've also been rather bad at consistently tracking it. 

Recently I implemented a [blogroll](/blogroll) on the website using a YAML file to store the info about the entries. It inspired me to start working on adding pages for media I've consumed or collected over the years and maybe get into the habit of tracking personal data again. There are many other people who run personal websites where they share their book and anime logs and have always enjoyed looking at pages like that. With that in mind I just want to share my thoughts about it.

## Why Collect the Data Anyway?

As said before, I love data. There are some practical-ish reasons for that and some less practical ones, but at the end of the day I want to collect that info.

A few core reasons though for self-justification:

1. Data is useful. You can find patens, supplement your memory, and make more informed decisions. It can make life easier for me.
2. Big tech and the government collect it so why can't I? Might sound silly, but I'd rather have a copy of my data to play around with than just leave it to all those big tech companies. It really ties into the [IndieWeb](https://indieweb.org/) philosophy of owning your data.
3. I like data visualization. It is equally silly as the second one, but I like graphs, charts, and the like. They are fun to look.
4. It promotes introspection. Externalizing what I think and logging what I do makes it taggable and observable.
5. I can share that data. More on that next.

## Why Display that Data Publicly?

I love reading other people's bookshelves, game lists, or whatever else they share online. I don't think over sharing is a good idea, but knowing what media someone has consumed really helps you get an idea of who they are and builds up that parasocial relationship before it has even begun. 

It also helps me find new things to read or watch. 

I'd like to imagine that someone out there might one day see my site and think "Oooo, that sounds interesting. I'll read it because I trust this guy's opinions".

Another reason is that it gives me a little more control over my public data in general. I can choose what to make public and to who. I can quickly inform a friend who is complicating a gift about what I already have or share a wish list. I can tie the daily weather to each blog post when I post it. I could go as far as [Aaron Parecki](https://aaronparecki.com) and share my [location](https://aaronparecki.com/gps/) (I won't) with everyone.

## What I want to Track

Ideally I'd track everything that is remotely useful to me, have a custom application that displays that data, and what have you. In the real world I can't do that without a lot of work or trusting big tech. Neither of those are things I'm going to do.

With that in mind I want to start with my media consumption.

### Anime

I've had a MyAnimeList account since Jan 13, 2013 and have regularly updated each season. With over 400 entries on my completed list you might start thinking I like anime and you would be right. As I want to [own my own data](https://indieweb.org/own_your_data) and not let it sit somewhere I don't control I've been slowly thinking up a way to list everything on this site instead.

I've already exported my list to XML as that is something MAL supports, but I'm thinking of using their API to automatically put everything into a nice YAML file to automate the process.

I could  make a bash script to process new entries and update old ones if I decide to not use MAL at all in the future.

One of my favorite things about MAL is it makes it easy to see similar media, find out how many shows you watched by the director, or find out what studio's work you have liked the most. It is very useful data for anyone who watches a lot of anime.

### Books

I used to have a Goodreads account, but quickly stopped using it after entering in a few books due to how clunky it felt. There is also the fact it is owned my Amazon. I shopped around for an alternative before giving up and not looking back. That was back when I was in high school (over 10 years ago), but the landscape hasn't changed.

The problem is it is hard to keep track of my reading history on my own. I used to put index cards in my books with basic info like when I started and finished them and a little score, but I stopped doing that when I started reading more short and digital stuff (all DRM free of course). The worst thing is when I go to a book store I always end up buying something and I've bought a copy of a book I already owned at least once.

The idea is to have a digital bookshelf where I can start logging my reading, books owned, and maybe recommend somethings to others.

### Video Games

I have a fairly large physical collection of Switch games. I am a firm believer in owning your media and this is probably the closest I am going to get. The problem is that the list of games is larger than my little brain can keep track of off the top of my head. Having a collection page that keeps track of what I own, played, and enjoyed can be useful in much the same way as keeping track of books can.

### Movies and non-Anime TV

I don't watch as many non-anime movies or as much TV as many of my friends, but every once in a while I will see something that is truly amazing and it would be nice to have a reminder of what I watched and when.

### Tea

I started doing tea [reviews](/reviews) specifically so I could keep track of all the tea I drank, but I realized that writing full reviews for everything would not be possible. Instead I'm going to log all my teas, short impressions with a score, tag them by type, and link to where I can get them. This way I don't have the problem of trying to think about what that amazing mint tea I had 3 months ago was.

### Personal Data

I do want to track my location, sleep, and mood again. I won't be publishing it on my website obviously, but it could be useful for the future. I'd like to be able to tell my doctor when I am sick, what the temperature was, how long I slept the night before, etc.

I think that is what the people who actually ascribe to the Quantified Self movement are about. I don't fully buy into self science with the limited knowledge I have, but it could still be useful info.

## How I'm Going to do it

To tell the truth, I'm not 100% sure yet. If you have ideas please share them. 

I have a few notebooks and I have this website. Like I said earlier in this post, I might write a script to help automate the process of data entry. I have tried using Logseq for logging PIM data before and tracking my reading for a few books, but it never took off.

Really the only way to find out is to try things out and see what sticks.

First thing I want to do is get that tea page done. This is TechTea after all.
