---
authors: 
- "Matthew Lamont"
categories:
  - Introduction to Computers
  - Tech Tips
date: 2022-01-01T17:20:27Z
featuredImage: ./img/readDoc_featureImage
tags:
  - Productivity
  - Tutorials
title: Reading Documentation | Finding Answers Online
aliases:
  - /reading-documentation/
slug: /reading-documentation/
---

> _Read the Manual_
>
> -- First answer to your technical question.

If you've ever asked a technical question online before you've probably come across this at least once. You don't know how to do something so you ask online and only get angry replies that don't help. Often you worded the question incorrectly or did not know the forum's culture, but there is a great way to avoid these issues to begin with: Read the Manual. Today we will learn how to read technical documentation the right way and avoid headaches.

## What do you want to know?

Before we can even get started we have to figure out what we want to know. Documentation can take many forms so it is important to know what we are looking from the start. You might not even know what you don't know so this step is really important.

Your first step is to get a basic understanding of what you're working with.

### Ask yourself "how familiar am I with the subject?"

If you are completely new you will want to look at tutorials first and technical documentation after you have a good understanding of the basics. Many things have tutorials alongside the technical doc on their website so make sure to check with the source first. When I set up my home server I didn't know anything about TrueNAS so I looked up a tutorial first. It gave me the basics of everything I needed to get it up and running.

Technical documentation is often concerned with specific functions, this means you will often not find information on how different features interact with one another form docs. This means you might need to connect some dots on your own or find examples of the specific interaction you are looking for. 

If you just want to know how a specific function works then that is where documentation is handy. When I needed to setup a Virtual Machine on my TrueNAS server I looked at the documentation on how to use that specific feature rather than a tutorial because I just needed that information. Tutorials are often full of extra filler and examples that aren't needed if you just want very specific information.

## Reading the Documentation

{{< figure src="./img/readDoc_SugarCubeForLoopDoc" alt="Sugarcube Docs Image">}}

You will often find official documentation for a program, language, or piece hardware from its official website. Some documentation is better than others though and some assumes prior knowledge, this is where tutorials and a notebook come in. If you find some terminology you don't understand write it down, look it up if you still don't understand it after following the examples and reading the docs.



Let's take Twine 2's popular story format SugarCube 2 as an example as it is well documented. Maybe we want to learn how we can iterate over some values in an array. If so we can look at the [documentation for a for loop](http://www.motoslave.net/sugarcube/2/docs/#macros-macro-for).

SugarCube's docs assume we have familiarity with Twine and other SugarCube concepts that were mentioned previously in the docs. Fortunately that makes it easy to know where to look for other info.

### Introduction

{{< figure src="./img/readDoc_SugarCubeForLoopDoc_intro" alt="Sugarcube Docs Image">}}

The documentation starts with the code we are going to use along with its structure. Most programming docs are structured similar to this. In SugarCube's case it shows us the 3 forms that a for loop can take as well as a line telling you it repeats its contents.

After that the docs gives you a brief history of the feature. This is very important in documentation that makes frequent changes that may not be backwards compatible or have been depreciated. Some software will have different versions of the whole doc with a dedicated change log instead of telling you inline what has changed, but sugarcube keeps it easy for us.

There is also a section that gives us some developer notes. This is not something I've seen in a lot of docs, but you might see this in documentation aimed at complete beginners.

### The Details

{{< figure src="./img/readDoc_SugarCubeForLoopDoc_details" alt="Sugarcube Docs Image">}}

The introduction to the For Loop said there were three forms so there are two subsections, one for the conditional forms and one for the range form. Lets focus on the Conditional form.

We are given a explanation on what it does. In this case it repeats whatever it contains as long as the condition is true.

Next we are given a quick warning about some limitations and where we can find more information about it.

Then there are the Arguments. Arguments are like options to functions in programming languages. This is something that all good documentation will tell you about. In this case we have three arguments and all of them are optional. We are also told where we can find info if we do not know something like how variables work.

This is great and all, but how do we put that together if we never seen it implemented before?

### Examples

{{< figure src="./img/readDoc_SugarCubeForLoopDoc_examples" alt="Sugarcube Docs Image">}}

Good documentation will give examples. In this case we are shown the setup for the 3-part conditional form of a for loop. There is documentation showing the setup of the array the loop is going to iterate over, the actual array itself, and the results.

This should give you a firm enough understanding of how it works so you can start experimenting. 

## Documentation is not Always so Good

SugarCube has great documentation, but it is not always the case. Bad documentation will leave you confused. This is where you will need to fall back to tutorials, experimenting, and asking good questions online. 

Next time we will discuss how to ask good questions online so make sure to follow us on social media and [subscribe to our RSS feed](https://www.blog.mattlamont.com/rss-our-information-diet/)
