---
title: "September 2026 Review"
date: 2026-10-01T08:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Monthly Favorites
  - Monthly Review
slug: /sep-review/
keywords:
  - Review
description: Another month full of stuff to share.
---

I've done quite a lot this month now that I think about it.

This website is it is now using Hugo 0.163.3, it was using 0.151 before. I always use the newest version of Hugo available in my Linux distro's repos locally, but I'm very slow to update the Netlify config as I really don't like breaking things. I've finally fixed all the random deprecated function names (Hugo really needs to stabilize their API, they really love to rename functions) and removed random bits of HTML from old articles. I'm officially without any errors in my Hugo output at the moment. I've even added updates to articles that reference deprecated Hugo functions so they should still work.

My partner was in a play and I got to see it. She played the only happy character in Abstraction by Daniel Adams. She played her part very well. This was for her acting school(Stella Adler)'s play festival so there were three other short plays I watched: Queens without a Crown (no author was given, but it was a collection of stories about women who were raped during what sounds like the Yugoslav Wars and how they lived with the trauma), and The Anniversary and The Proposal by Anton Chekhov. While the first two plays were very dark, the overall experience was fun and I loved seeing my partner demonstrate her acting skills she has been working hard to develop. Often her events line up with days I'm on call or otherwise busy so I'm overjoyed that I got to her debut play.

I also got an Elgato Stream Deck. It is basically a macro pad where every key has a screen so you can easily know what each button does in context of a given situation. As there is no native Linux version of their software and I'm using NixOS there have been some hoops to jump though, but it is really cool so far and I'll be sharing some of my discoveries in a future post. Got it for real cheep too and wanted one for over a decade so I'm a little more than happy to be able to play with one now.

Didn't end up going on a trip with my parents this month like planned, we will likely go sometime near the end of the year or at the start of next assuming we are still all alive then.

## Things I Learned

With the goal of making the Stream Deck useful, I had to learn some new Linux programs/terminal commands.

WirePlumber Control CLI lets you control and monitor PipeWire inputs and outputs. Very useful if you want to change audio outputs at the push of a button or in a script. I've been using `wpctl set-default <device-ID>` to set the audio device. I still have to dive into it a little more as some things don't seem to be consistent, but learning is part of the fun.

`playerctl (1)` has been another big player in getting things working. The media player plugins for the StreamDeck don't seem to be working on my setup so I basically replaced them with `playerctl`. The program lets you control any media players that support MPRIS (most of the good ones). You can specify the specific player among all the ones running, but it also defaults to the last active one and that is how I've been using it.

## Blog Post I Made

So earlier this month I made a [post about Omarchy](https://techtea.io/articles/2026/omarchy/), a popular collection of Arch Linux config files created by DHH and funded by other fascist and alt-right adjacent folks. During my research I've found quite a bit of other people's articles highlighting the problem and why it matters so much that we prevent people like DHH from holding power in FOSS.

Here are some of them:

- [Brennan Kenneth Brown's Stop Omarchy](https://stopomarchy.neocities.org)
- [Nicco Loves Linux's Why are Billionaires Funding a Linux Distro?](https://www.youtube.com/watch?v=0LN-kvr32K8)
- [Jordan Petridis's DHH and Omarchy: Midlife crisis](https://blogs.gnome.org/alatiera/2025/11/06/dhh-and-omarchy-midlife-crisis/) - I don't fully agree with the tone here on all points of this post, but still gives some good background info.

## Video Games

No Man's Sky had their 10th anniversary event. Every few months they have these events called Expeditions that players can participate in. They often have unique mechanics and have you start with a fresh character. They have multiple milestone objectives and once you've completed them you go back to your primary save and can collect rewards for that particular Expedition. This time around it was going through all the major updates to the game where you would do an activity related to that update and receive audio developer commentary. The whole experience was really fun as a newcomer to the game. I knew the game came a long way, but it is really cool to actually see it. There were some bugs and annoyances with it, but ultimately well worth jumping back into the game for. The Expedition made me interact with mechanics I've never touched before so now there is more for me to do when I jump back into the game in the future. The rewards were cool too.

I played a little more Atelier Resleriana: The Red Alchemist & the White Guardian, but not much. The characters are charming, but I feel like I need to be in a particular kind of mood to play this game and more so than Atelier Sophie. Maybe I should go back to playing Sophie and finish it instead.

I also played Splatoon Raiders. Shooters are not normally my cup of tea, but this one has just the right blend of Nintendo weirdness and thoughtful gameplay to make me want to play it. Gyro controls are strange to me, but do make aiming easier on the Switch's awkward joycons, I wish they let you use both the analog stick and gyro at the same time to aim instead of one or the other in the settings. There is a good mix of easy and challenging levels and apparently late game stuff is very challenging according to reviewers. The game also didn't hold my hand too much, rare for games to respect players that much these days. Makes me hopeful for the future. Anyway, this game is pure fun for some types of people, my partner has been stealing the Switch 2 she got me for my birthday last month to play it. This is my first Splatoon game as I'm not a multiplayer type of person, but I can see why people like it. Still won't see me going out of my way to play the other games in the series though.  

## Links

### Projects

[Steven Bennett](https://www.youtube.com/@StevenBennettMakes/videos) has been showing his development process of an open source task light based on the Dyson Solarcycle. I've shared his YouTube videos multiple times before, but now the project is complete. There is an [announcement video](https://www.youtube.com/watch?v=ipVFRH6TQfM), a [github with the files](https://github.com/stevenbennett/Open-Task-Light), and a website where you can [buy kits to build your own](https://opentasklight.com). If I had a little more money I'd buy one as it looks awesome. Even if you are not interested in owning one you should check out his YouTube channel as the build logs really show the thought process and hard work that goes into making something. 

[OpenDeck](https://github.com/nekename/OpenDeck) is a FOSS program for using the Elgato Stream Deck hardware on Linux. It is very cool and while I had issues getting plugins to work on NixOS, most can be recreated using terminal commands. 

### Articles

Vaxry, the creator of Hyperland and other cool tech, wrote a great article about [his thoughts on AI and digital literacy](https://blog.vaxry.net/articles/2026-aiIsABitDifferent). While Vaxry may be more than a little abrasive online, especially in his earlier years, I pretty much agree with his post. He is more pro-AI than I am, but he emphasizes how computers and AI are different from prior tech in that we do need to understand them or we will be used by them. You don't need to know everything about a hammer to use it effectively and a hammer will not try to manipulate you into voting for someone who will hurt you. Tech companies on the other hand will use every trick in the book to harm you and AI is vastly increasing their toolbox. You don't need to like tech or understand every part of everything, but you do need to know the basics of how it all works and why. He also mentions helping others create maps for navigating the tech we interact with daily, that is something I completely agree with. I will note that Vaxry might posibly be in bed with alt-right people and Hyperland is getting money from Omarchy, but I don't think that makes this particular article invalid.

Kev Quirk wasn't always a writer, but [one day he decided to improve his writing skills and he did](https://kevquirk.com/its-never-too-late-to-learn) he also [recently got into fountain pens](https://kevquirk.com/using-fountain-pens-for-note-writing). It is never too late to learn new things and it is always good to follow your curiosity. 

Ana Rodrigues writes about [her experience with the IndieWeb, the value of a personal website, and the digital community that forms around it](https://ohhelloana.blog/mkdn/). It is always fun to read other people's perspectives of online community. I'm a lurker and almost never post publically outside this blog or reach out to others before they reach out to me, but I love talking to people and listening to their stories. Ana is much more outgoing on the web and has an amazing website that is worth giving a look at.

Derek Sivers talks about [what it means to be a good citizen of the internet, a netizen](https://sive.rs/netizen). The internet used to be a bunch of nerds freely sharing tools and knowledge with anyone who wanted them. There were always a few odd balls who wanted to make money or gain social capital using the internet, but that wasn't the point for most people. Nowadays much of the internet has been poisoned by capitalist greed, but it isn't like the old internet is gone. If anything a mix of nostalgia and pushback against the hyper consumerist internet has made the idea of what the old internet was like even more real and stronger that it ever was in the past. Derek and many others contribute to this wonderful place we call the internet and make it a better place for everyone who seeks to be free from the corporate bubble. 

Marisabel Munoz writes about [the courage it takes to write and publish publically, especially in the AI age](https://marisabel.nl/public/blog/The_Courage_to_Write). There really is something lamentable about the change from wondering "How did they come up with that?" to "Is this written by AI?". Those of us that are more AI adverse pick up more easily on when things are AI generated, but that also means it is easier to be skeptical of real writing. With that in mind it is scary to write in an environment like that. Not only am I not nearly as good of a writer as Marisabel is, there is a fear that someone will mistake the writing I spend hours (sometimes days) on as some mindless AI slop. Genuine criticism is already hard enough without people questioning if you are human. It takes a lot of courage to write and always has, but nowadays, creation is an act of defiance and is more important than ever. Even if it is scary, we can all create and have the power to share that creation with others. 

### Videos

Tom FitzGerald talks about [the history of conquest and how it became wrong](https://www.youtube.com/watch?v=oSEj-y957Xc). It is pretty interesting. Even going back to ancient times not everyone necessarily believed that conquest for its own sake was moral, but over time the justifiable reasons for conquest shrunk and nowadays, we don't really see much in the way of noble conquest. Even when countries like the U.S. perform imperialist actions they usually do not "conquer" countries because it simply is not justifiable and looks bad nowadays. Tom talks about the Roman perspective and it is pretty interesting. Well worth a watch.

Nicole Rudolph explains [what IQ is, how it has been measured in the past, and how it is misused](https://www.youtube.com/watch?v=HH-lY2tkRHI). As much as I love the idea of the quantified self for fun (putting numbers or stats to oneself and tracking it), the idea of applying that to others or having someone apply that to me is awful. IQ has been used to justify all manner of horrible things. We aren't talking random online "IQ tests", but the real ones. It is a noble goal to try reaching people on their level when trying to teach them new ideas or create a more equitable society, but IQ is often used to justify intellectual elitism and punishing people who do not do so well in the areas IQ tests track. Nicole's video is great if you want to know the history of it and why it is so awful in application. 

## See You Next Month

I'm a bit tired this month. Work and personal life has been very busy and most of my free moments were spent taking care of myself though the power of video games. That meant I didn't write or spend as much time on the internet as normal (probably a good thing). 

Truth be told, I really have been out of touch with my hobbies lately. Going to do a nice reset and spend a weekend working on a project or tinkering with stuff.

Anyway, let me know how your month has been. Hope October will be a fun one for you.