---
title: Open Source Productivity Tools to Organize Your Life
date: 2023-05-09T17:45:59Z
draft: false
authors: 
- "Matthew Lamont"
categories:
  - App Spotlight
  - Tech Tips
featuredImage: ./img/open_source_productivity_apps_cover_image
tags:
  - Cross-Platform
  - FOSS
  - Logseq
  - Nextcloud
  - Note Taking
  - Open Source
  - Productivity
  - RSS
  - Thunderbird
  - App Spotlight
aliases:
  - /open-source-productivity-tools-organize-your-life/
slug: /open-source-productivity-tools-organize-your-life/
keywords:
  - productivity
description: Unfortunately most productivity software is privacy invasive and expensive. Today we are going to cover some free and open source alternatives.
---

If you have ever seen a productivity video on YouTube, you've probably been recommended a bunch of proprietary tools to help organize your life. The problem with these tools is that they are a black box, usually controlled by a big tech company, and productivity tools often include every aspect of your life. Today we are going to discuss [free and open source tools](https://www.blog.mattlamont.com/what-is-free-and-open-source-software-foss) that both respect your privacy and help you keep track of life, no matter how busy you are.

## 1. Nextcloud - A Productivity Powerhouse

[Nextcloud](https://nextcloud.com) is a behemoth of an application that has had a huge impact on how I interact with the internet, my computer, and my phone. It is a cloud storage application that has effectively replaced Google services in my life since I started using it.

Nextcloud is self-hosted, or you can find providers that will host it for you. However, that costs money, so I will try to include several alternatives to each Nextcloud app that I use.

### Nextcloud News

{{< figure src="./img/open_source_productivity_apps_nextcloud_news-1" alt="Nextcloud News Image">}}

Nothing improves productivity like a RSS reader. [I've talked about them before](https://www.blog.mattlamont.com/rss-our-information-diet/), but basically a RSS feed provides a chronological list of posts from a website. A RSS reader lets you collect these feeds into one place and then filter, organize, and read them. For this task I use Nextcloud News.

Nextcloud News lets me subscribe to news websites, YouTube channels, and blogs I read. This is important because many websites are designed to keep you stuck in an endless feed of content. When you control the feed, you are much more likely to be able to take control of the content you consume.

[Feeder](https://f-droid.org/packages/com.nononsenseapps.feeder/) is another RSS reader that is available on Android and has a great design. I'd recommend it if you decide not to use Nextcloud.

### Nextcloud Calendar, Tasks, and Deck

Every good productivity system needs a way to manage tasks, sometimes multiple ways. Fortunately NextCloud has us covered here. These 3 tools each do slightly different things, but are related. This is not an article about productivity systems, but I will try to explain what ways I use them.

#### Calendar

{{< figure src="./img/open_source_productivity_apps_nextcloud_calendar" alt="Nextcloud Calendar Image">}}

The Calendar gives you exactly what it sounds like, a calendar. What makes it special is that it can sync to any calendar app that supports caldav, so I can sync it with Thunderbird on my computers and most Android Calendar apps. I put events, reminders, and block out time with my calendar. I split it into several different areas in my life and use Nextcloud to color code them so I know at a glance what they are for. 

For an alternative you can use your phone's calendar or Thunderbird to manage it.

#### Tasks

Unlike events, tasks are actionable to-dos and thus need a to-do list. Tasks is Nextcloud's to-do list tool. I use tasks for my to-do lists. This could be reading a book, doing a one off chore, or setting up an appointment that will then become an event in my calendar. I have separate lists for different areas of my life the same as my calendar; this lets me have tasks for this blog, a reading list, etc. Tasks can be synced over caldav so they can be synced with many to-do apps on your phone and Thunderbird on desktop.

An alternative to this could be Thunderbird on its own, or a PKM system like Logseq. I will talk more about that soon.

#### Deck

Deck is a tool that I'm still getting into, so I don't use it often, but it lets you organize your tasks into a Kanban board. For those of you not familiar, a kanban board lets you move tasks between different states. A simple one could be To-do -> Doing -> Done. It lays these out in a way where you can see all your tasks and where they are at a glance.

As an alternative you can also use Logseq, as it has a Kanban plugin.

### Contacts

{{< figure src="./img/open_source_productivity_apps_nextcloud_contacts" alt="Nextcloud Contacts Image">}}

A good contacts list is important for any productivity system. This is where you keep track of who you know and organize them into categories. The best way to remember a number is to have your phone remember it for you.

By default, your phone probably syncs your contacts with either Google, Samsung, Apple, or some shady Chinese company. This is not really great for your privacy and is also a violation of your contacts' privacy. Fortunately Nextcloud gives you a way to sync contacts between all your devices. The best part is that you can sync these contacts between not only phones, but any app that supports the vcard format.

For alternatives, you can use the phone app built into your phone or any address book app on f-droid and keep the contacts local only. You could also use Thunderbird on its own if you just want to keep track of people on your computer.

### Nextcloud is a FOSS Productivity Powerhouse

It might be hard to justify, but if you can afford to install it on an old computer you are willing to convert to a server, or if you have a decent NAS laying around, Nextcloud is king. I run a copy on my home server. I also pay about $50/year for a 50GB instance of Nextcloud that is hosted by a provider, so if you don't want to worry about self hosting you can still get the benefits.

Unless otherwise noted, these Nextcloud tools all work in the web and either integrate with existing desktop and android apps or have a dedicated app. All Nextcloud features are accessible via a web browser as well.

## 2. Omnivore - End the Endless Scrolling 

{{< figure src="./img/open_source_productivity_apps_omnivor" alt="Omnivor Read-It-Later Image">}}

Even with our RSS reader we are still going to get distracted by random things we see on the internet, this is where a read-it-later app like [Omnivore](https://omnivore.app/) comes in. Think of this kind app as glorified bookmark tools combined with a digital book reader. 

Instead of opening the thing you randomly seen a new tab, consume it, go to the next thing, and then forget what it was you clicked on 15 minutes ago, a read it later app lets you click a button in your web browser or a mobile app to save the article for later. Then you can read it or delete it when you are in a better state to consume content. Omnivore also gives you the ability to highlight and take notes on content you save, as well as sync it with PKM software like Logseq

When we are in information gathering mode, we are usually bad at actually consuming or judging the quality of that content. This is another tool that helps us break free from the never ending stream of content that saps our attention span and our productivity.

## 3. Logseq - Advanced Note Taking

{{< figure src="./img/open_source_productivity_apps_logseq" alt="Logseq PKM and Notes Image">}}

[Logseq](https://logseq.com) is a Personal Knowledge Management tool and note-taking app that has become my go to note-taking app. Logseq gives you a non-linear way of taking notes, capturing information, and referencing the notes you take. It works on all major platforms including web, though all your notes are saved locally.

What sets Logseq apart from tools like Joplin or a bunch of text files on your hard drive is how it links ideas together. Instead of your notes being stuck in a rigid hierarchy, they are linked bidirectionally between each other. The program uses the idea of taking atomic notes that are easily reference-able, so you actually use and read them for years to come.

Best of all, there is no vendor lock in. All of your notes are written in either plain markdown or in org, so you can take your notes with you if you change apps.

Logseq is a bit complex, so it will take a few articles on our part to fully cover it and how it will boost your productivity. There is a wonderful YouTube video series by OneStutteringMind on Logseg that you can watch [here]("https://www.youtube.com/playlist?list=PLNnZ7rjaL84JjFpgDxRlAOKRa9ie25gtp). Once you get the hang of using it, you can customize it with plugins, scripts, themes, and integrations with other applications.

## 4. Thunderbird - Email Productivity King

{{< figure src="./img/open_source_productivity_apps_thunderbird-1" alt="Logseq PKM and Notes Image">}}

[Thunderbird](https://www.thunderbird.net/) is a desktop email client, calendar, and RSS reader. I use Thunderbird to check my emails across all my accounts and sync info with Nextcloud. What makes this particularly useful and productive is that I can create advanced filters in Thunderbird that can sort my email, view all my email addresses in one place, and tie my contacts and calendar into the same application.

If I get an email from my friend that includes a calendar invite, I can have Thunderbird place that invite on my calendar, send a response email, and sync it all with the rest of my devices with Nextcloud. 

Thunderbird has many extensions that can further increase your productivity: unified inboxes, file sync with Nextcloud, etc. Give Thunderbird a try if you use more than one email address.

## 5. Kontact - PIM for KDE Users

{{< figure src="./img/open_source_productivity_apps_kontact" alt="Logseq PKM and Notes Image">}}

While I use Thunderbird for most of my desktop calendar and email needs, KDE has an application suit that does everything Thunderbird can and more. [Kontact](https://kontact.kde.org) is a user interface that combines several KDE applications into one place for all your productivity needs. This includes email, contacts, calendar, to-do lists, RSS feed reader, note taking, travel itineraries, and more. This creates a collection of applications that is great for Personal Information Management (PIM), not to be confused with PKM like logseq (that is a future article).

What sets Kontact apart from Thunderbird is how modular it is and how it integrates with the KDE desktop. For example, if you don't want the mail and to-do apps, you don't have to install them. However, you can still get your calendar and RSS feeds. Your contacts and calendar can integrate with the calendar widget on your panel as well as other KDE apps. There is so much power here. It also integrates with NextCloud.

I don't use it much, as Thunderbird serves most of my needs and Kontact used to be unstable when I first used it, but I am starting to come back to it. It's worth taking a look at it and seeing if it fits your needs.

## FOSS Productivity Software Exists and it is Great

Many think that there is no good productivity software in the open source world, but the truth is that there are many applications that can help us take control of our lives and be more productive so we can focus on the things that mater to us. It's just a matter of finding the right one.

Please let us know what your favorite Free and Open Source apps that help you be productive are.
