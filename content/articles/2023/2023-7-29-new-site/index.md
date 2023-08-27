---
title: "2023 Website Update"
date: 2023-08-04T09:48:27-07:00
draft: false
authors: 
- "Matthew Lamont"
categories:
- Website Update
featuredImage: 
tags: 
- Website Updates
slug: /website-update
keywords: 
- WordPress
- Hugo
description: "We rewrote the website in Hugo. Here are some of the reasons we moved away from WordPress."
---

It may be the middle of the year, but I went down the rabbit hole known as the [IndieWeb](https://indieweb.org) and converted this website over from WordPress to using Hugo. The site still doesn't support webmentions yet but that will come eventually. It was not an easy process to convert everything, but I think it is all working now. I have a more in depth article in the works now on how I did it.

Another thing you will probably notice about the website is the new domain name and content organization. All the old blog.mattlamont.com links will redirect to their page here on techtea.io.

I'm still figuring out the layout for all the content, but from now on I will be splitting short-form content from long-form content. This should make it easier to find things and also encourage me to post more frequently.

## Why Rebuild the Website?

So I've used WordPress for my website since it started back in 2013. It was easy to use at the time and did what I needed, but it was always clunky and slow. As time went on and I learned more about blogging I learned about SEO and WordPress's UI encouraged me to use lots of images. Over time WordPress got even more cumbersome to use. It is a great tool if you have 50 employees or need a website that is easy to configure for non-tech people. It is overkill and limiting for individuals running small sites as a side project. I'd even say it is limiting for websites with hundreds of employees under some circumstances.

### SEO

I'm a firm believer in optimizing your content to be both human and machine readable. I provide the human text they can easily read and the machine metadata describing my content so it knows how to rank it. The problem is SEO principles promote bad writing.

A lot of search engines enforce limits on paragraph size, keyword density, and a lot more. None of that is metadata and Google, Bing, and Brave Search should not care how my content is structured. I gave them what they need to know, I even have an RSS feed if they don't want to parse my HTML.

My hosting provider encouraged the use of a SEO plugin that would help with the optimization process. It would give an SEO and a Readability score based on how you write the article. Useful if you want to write like every other website out there, but it always made me double check my writing and change it to match what the plugin though was good writing.

Now you might say "Just disable the plugin or ignore it" and you would probably be right. The problem is without the plugin it was hard to add the metadata for the pages and ignoring it was hard otherwise I would not complain. There was a Readability and a SEO Score for every article that I would see every post.

Now I use a text editor to write my website. I don't have to worry about any of that other stuff and can focus on writing.

### Images

Everywhere I look online I see that I should have a hero/feature image for my blog posts. I should use lots of images to break up content. The advice would include links to stock image sites (some of which I used on this site). This encouraged a lot of unnecessary images. This would slow down the page loading times, distract me from the writing process, and downplay the importance of the useful images on the website.

From now on I'm going to try to stick to only necessary images. I might not even use the feature images anymore. I can create visual distinction in other ways that can show up in even text based browsers. The website will load a lot faster too thanks to that.

### Clunkiness

WordPress has a great editor for quickly making layouts and inserting media, but actual writing was a pain. The interface would lag sometimes, you had to use the mouse to change features of the blocks, and if you wanted to just use Markdown you had to use plugins or copy and paste content that you would later have to edit anyway. Adding features required plugins or themes that add complexity and might stop being supported at a moments notice.

With Hugo all my content is in Markdown, a plain text format. This means it is easy to use, portable (if I ever want to move away from Hugo), and fast to write. I would put off writing ideas just because WordPress would slow me down. Now I am blazing through this article and have two more in the works.

Hugo generates static HTML, CSS, and JavaScript so it is easy to add new feature. Hugo's templating tools make it easy to add new features to the site, prototype themes, etc. The theme I'm using now was missing some things I wanted and I was able to quickly make those changes. In the future I plan to add more to the site thanks to Hugo's easy templating tools.

## It isn't WordPress, it's me

None of these issues are really WordPress's fault. I was using the wrong tool for the job. WordPress was built for making large, media heavy, websites.

My website however is mostly text and hyperlinks. I write for humans and not SEO. I don't do well with distractions and UI elements that promote a particular way of writing. Well now I have a website that works with the tools I use everywhere else. This website is lighter weight (WIP), easy to maintain, and hopefully easier to read.

## What now?

I plan to explore more of the fantastic sites on the IndieWeb for inspiration and continue to write about what maters to me. More content about [FOSS]({{< ref "/articles/2021/2021-01-14-what-is-free-and-open-source-software-foss">}}) [Software]({{< ref "articles/2023/2023-05-09-open-source-productivity-tools-organize-your-life">}}), Digital Freedom, and more will be right around the corner. Also expect this website to change frequently as I love tinkering.