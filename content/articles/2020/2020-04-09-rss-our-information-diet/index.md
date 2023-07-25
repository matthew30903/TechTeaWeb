---
author: Matthew
categories:
- Introduction to Computers
- Tech Tips
date: "2020-04-09T18:22:30Z"
featuredImage: ./img/RSS-Cover.jpg
tags:
- FOSS
- Open Source
- Productivity
- RSS
- Thunderbird
title: RSS | Our Information Diet
aliases:
  - /rss-our-information-diet/
slug: /rss-our-information-diet/
---

RSS is a tool that solves one of our greatest problems in our connected world: information overload.

## What is RSS?

Really Simple Syndication (RSS) is a standard protocol for websites to share information with other sites and applications. This is used by blogs and news sites to share their content in an accessible way. Thanks to this standard, you can subscribe to a website's RSS feed and get updates as new content becomes available.

## Why Should I use it?

Imagine you are someone really interested in technology. You frequently check several tech blogs (including this one) and some YouTube channels. There is also a store on Etsy that you love and must have every one of their products. You check every week for updates. Unfortunately, you have trouble keeping up because:

* Some sites update so infrequently you feel like you're wasting your time when you see no new content.
* There's that one columnist on the New York Times you really love, but there's just too much noise with all the other news.
* You end up overwhelmed by all these sites and start to forget creators you love.
* You end up seeing the same information whenever a new trend hits the tech world

RSS and a little work on your part can fix these issues. Not only can you get notified when there's new content, but you can filter this information at a glance.

Many RSS readers and tools also aggregate content based on interest. This can help you find more content that is relevant to you.

## Getting started with RSS

The first thing you need in order to filter your information intake is a Feed Reader or News Aggregator app. RSS is old technology, so there are many to chose form.

[Feedly](https://feedly.com/i/welcome) is one of the most popular readers on the market, and supports web and mobile platforms.

{{< figure src="./img/feedly_main_ui.png" alt="Image: Feedly Main Feed">}}

Feedly already has an excellent <a rel="noreferrer noopener" href="https://blog.feedly.com/get-the-right-content-on-your-feedly/" target="_blank">tutorial on their website</a>, so we won't cover too much here. Unfortunately, advanced filtering of your feed is limited to a payed account. You also have to trust an online service to not filter your results and respect your privacy. If all you want is to curate your news by source, this is a great way to do it.

If you need more power and a healthier relationship with you phone, you can use a desktop news client. The two desktop clients I will be covering today are Thunderbird and QuietRSS. Both applications follow a similar approach to RSS.

### Thunderbird

[Mozilla Thunderbird](https://www.thunderbird.net) is an email client, calendar, and news reader. You won't have much trouble if you already use it to organize your emails. It comes pre-installed in many Linux distros and is available on all desktop platforms. There are better options, but Thunderbird will serve most user's needs.

To add a RSS feed to Thunderbird, you will first have to make a Feed Account. Click the Menu -> New -> Feed Account... and then name your RSS Folder. 

{{< figure src="./img/thunderbird_add_feed.png" alt="Image: Add a Feed to Thunderbird">}}

Click on your account folder to add and manage feed subscriptions. It's rather straightforward; you take the URL of a feed and paste it into the Feed URL box, chose the folder you want to store the articles in, decide if you want to load the whole article or only a summery, and how often it should check for updates. 

### QuietRSS

[QuietRSS](https://quiterss.org/en/download)</a> is a free and open source desktop RSS reader. Quiet is simple and easy to use, as it is a dedicated RSS reader. It also has an integrated web browser for viewing articles from the source, something Thunderbird lacks without extensions. It is available for Linux, Mac, and Windows.

{{< figure src="./img/quiet_rss_add_feed.png" alt="Image: Add a Feed to QuietRSS">}}

You can click on the Plus icon to add a new article to your feed in Quiet. Then select Next to pick a folder to store your feed in.

You can add Random Thought's RSS feed using this URL: <a rel="noreferrer noopener" href="https://www.blog.mattlamont.com/feed/" target="_blank">https://www.blog.mattlamont.com/feed/</a>

## Filtering Messages

Now that you have narrowed down your news sources, you might be thinking "We're finally done!" and you could be right. If you're happy with what you see in your feed and can quickly glance at titles to filter content yourself, then we are done. Filters, though, can help you refine your feed and help keep information overload at bay. 

Both Thunderbird and Quiet have very similar filter support. The main difference is Quiet lets you filter by feed if so desired. 

{{< figure src="./img/rss-filters-quiet-thunderbird.png" alt="Image: QuietRSS and Thunderbird Filters" caption="Quiet (left) and Thunderbird (right)">}}

You select a condition like Title/Subject contains Zoom, then an action such as Delete. Filters are rather simple, but can be very useful.

## Find RSS

RSS is all around us on the web. Blogs, news sites, and even subreddits have RSS feeds for you to subscribe to. Some useful places to look are:

* [BBC](https://www.bbc.com/news/10628494)
* [New York Times](https://archive.nytimes.com/www.nytimes.com/services/xml/rss/index.html)
* Add .atom to the end of GitLab and GitHub repos for that repo's RSS feed
* Add .rss to the end of a reddit url for that page's RSS feed.
* Add a YouTube channels using the following URL: https://www.youtube.com/feeds/videos.xml?channel_id=  
Enter the channel ID after the equals sign.

## Take Back your Life with RSS

In this day and age, we are bombarded with content. RSS helps us control that content, filter it down, and find what maters most to us. With RSS, we can cut the time we spend looking at the news, help avoid bias algorithms and Facebook filters, and develop a healthier relationship with the content we chose to consume.
