---
title: "March 2025 Review"
date: 2025-04-01T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Monthly Favorites
  - Monthly Review
slug: /mar-review/
keywords:
  - Review
description: A lot has happened this month. Lets go over what has been going on in my world and share some fun links. 
---

I tried to avoid the politics this month that didn't directly effect me or my friends. Not an easy thing to do when the idiots running this country are so comically evil, but I've done a decent job this time. 

One of my home servers went down due to a surge warning on one of the motherboard's USB ports. Took the opportunity to migrate from TrueNAS Core to TrueNAS Scale on both my servers. The migration process was much easier than I thought, though it broke my apps running in Jails. Going from FreeBSD to a Debian based backend with minimal issues is rather impressive. iX Systems has done a great job. It is a bit of a shame that they are pushing towards Linux, but I'm much more familiar with it, and it gives me more opportunities to learn Linux containers. While I'm dreading setting up Nextcloud again it gives me a great opportunity to fix the mistakes I made the first time.

There was a lovely blood moon eclipse on the 13th. It was midnight by the time it reached totality here in California. Unfortunately none of my friends saw it other than my roommate and girlfriend.

I took a Pilates class with my girlfriend this month. It was one of their intro classes to recruit new customers. My back felt better than I thought it could after the class. Might sign up for more once my budget allows for it.

I also visited my family in my hometown. There were many things to do, but only so much time when it is a 2-hour train ride and you only have a weekend to do it in. Hung out with a friend, played some MTG with my little brother, and spent quality time with the family. 

## Things I Learned

I have a LG Dualup monitor as my secondary screen. While it is amazing it has quite a few quirks. It is basically two screens stacked on top of one another without a bezel. One of the things that annoyed me was how KDE handles screen edges by default. If you move your mouse to the edge of a screen it will stick to the edge of that screen for a few moments unless you hit it fast. I treat the two halves of the Dualup as separate screens so I can do fancy things with my KVM, but when I'm using it as one large screen it becomes annoying. It turns out you can disable this feature by going into **Settings -> Mouse & Touchpad -> Screen Edges** and uncheck **Corner barrier** and set **Edge barrier** to **None**. Months of being mildly annoyed by this and it was an easy fix that took under a minute to perform.  

I've been putting some time into properly learning some shell scripting this month, only a few minutes here and there. I'm going to set aside time each week for some more deliberate practice in the coming months. 

## Games

Finished playing *Little Misfortune* (PC) with my girlfriend this month. We played through it twice to get what we think is the best ending. A short, bittersweet, adventure game that really punches above its weight. There are some problems with how it handles the tone mismatch between its dark humor and the main character's childlike innocence, but it is hard to fault it. There is a lot of heart in it. I recommend if you have a few hours and are alright with a story that touches upon death, coping with abuse, and a little horror with some over the top dark humor. The game worked perfectly on her Linux laptop.

I played a little of *Atelier Sophie: The Alchemist of the Mysterious Book* (Switch) to get myself ready for the Yumia release. I love the crafting system and the characters. The game is a nice slice-of-life RPG. I've not finished it, but considering that my last save before this month was over a year ago I'm not likely to finish it soon.

*Atelier Yumia: The Alchemist of Memories & the Envisioned Land* (Switch) was released near the end of the month. I'm just started getting into it. So far it is not as good as the other games I've played in the series and the performance is much worse, but we will see where it goes. The crafting system hasn't grasped me yet nor have the characters. It is more of a spinoff than a mainline game. I'm not expecting it to be like the others in the series, but the crafting system and character writing is extremely important for any Atelier game. I hope it isn't just open world for the sake of it and that the base building mechanics evolve with time. It also needs a patch to improve performance.

## Movies

I watched *The Day the Earth Blew Up: A Looney Tunes Movie (2024)* with my girlfriend in theaters this month. It was a fun movie and the big punchline joke was extra funny due to my girlfriend not liking a particular tea drink adorned with tapioca and milk. It is a good movie for what it is. There were times when the jokes fell flat and sometimes felt like it was trying too hard to be heartfelt. 

## Links:

### Cool Projects

[Labelle](https://github.com/labelle-org/labelle) is a program for interacting with DYMO label printers. I have a DYMO LabelManager 280 and have been using it with the built-in keyboard for a while. Labelle makes it so much easier to use. Now I can print QR codes, 2D bar codes, images, and use custom fonts. It has a GUI, but also works from the terminal when you need to script out your labels. 

[Anubis](https://github.com/TecharoHQ/anubis) is an anti-AI scraper tool that uses proof-of-work challenges to stop scraper bots from hogging your bandwidth. It isn't perfect, will destroy your search engine rankings and absolutely destroy user experience on your site, but it can help reduce the load on your server if you are getting attacked by bots. It breaks text only browsers and doesn't work well on low powered devices, so I'd not use it on my site, but it is a tool that might prove useful for some of you. Eventually AI will get around it, but it is a tool to help at the moment. Xe Iaso, the tool's creator, gives the details of how it works on their [blog](https://xeiaso.net/blog/2025/anubis/).

[LanguageTool](https://languagetool.org) is a nifty grammar checker. While there is advertising on their website that says it is an AI grammar tool it is actually a lot better than that and has existed long before AI hype made everything "AI". It uses an actual rules engine to help correct grammar and spelling. It seems they are experimenting with language models to help improve the system and that does make me skeptical, but we will see how it develops over the next few years. In any case, I've been trying it out for editing this article and hope it makes reading a little easier. LanguageTool is FOSS and can be self-hosted. NixOS made it really easy to get setup with it too.

### Articles

Cory Dransfeldt shared how to improve your [privacy on big tech platforms](https://www.coryd.dev/posts/2025/make-yourself-less-valuable-to-tech-companies) as well as a list [of privacy respecting alternatives to U.S. companies](https://www.coryd.dev/posts/2025/alternatives-to-us-tech-platforms#fnref4). It is more important than ever to avoid U.S. based companies when possible due to the increase in authoritarianism in the country, equally true for U.S. citizens like myself. 

Frills shared [the nice things people have said to her](https://frills.dev/experiments/nice-things-people-said/) in a cute and interactive webpage. 

Drew DeVault is writing a series on [intellectual property](https://drewdevault.com/2025/02/13/2025-02-13-On-intellectual-property.html). He starts by creating a working definition on how we attribute value to property and what intellectual property is in the first place. I look forward to reading more on the subject. My own stance on intellectual property is complex, but it stands somewhere on the side of information should be free, but LLMs/large companies should not be making money off the backs of other's intellectual labor.

Simone Silvestroni talks about how the advancements in tech, automation mostly, would have seemed cool a few decades ago, but [the goal of endless growth and wealth for a few at the expense of everything else has soured that](https://minutestomidnight.co.uk/blog/if-we-want-continued-growth/). Automation solves no real world problem without ethics behind it, right now AI and advanced robotics promise a future where the rich few don't need us anymore. Technology is cool when it serves a noble or geeky purpose. AI, Robotics, and even (arguably) Blockchain could have real world benefits, but as long as society rewards the asocial behavior of corporations and billionaires we will see more evil coming out of it than good.  

Diederick de Vries talks about [how dependent on GPS he is](https://thefoggiest.dev/2025/03/06/life-without-gps-sucks). It is very true, life without GPS isn't nearly as easy. GPS gives us so much both in the way of the useful tooling built around it and fun of collecting personal location data. Also, the shutdown of Mozilla Location Services was a major blow to location tracking in a lot of places. 

Ruben talks about those awful [POP vinyl figures](https://rubenerd.com/pops-and-collectables-for-the-sake-of-them/). I pray that they aren't as prevalent now over where Ruben is as they are over here. They are everywhere still, drowning out other figures and collectibles in general. Usually I say "you do you" when it comes to people's interests and hobbies, but POP collecting is where I draw the line, I hate those things. 

On a more serious note, Ruben also talks about what is going with the [United States under Trump from his perspective](https://rubenerd.com/australia-singapore-and-the-us/). As awful as it is to see what is happening from the inside, it is terrible for our (former?) allies. I pray that the United States will side with its allies when the time comes, but it is hard to hold faith when the president ignores laws and throws everyone under the bus.

Terence Eden shows his [collection of scripts for getting Kobo to somewhat automatically undercut Amazon](https://shkspr.mobi/blog/2025/02/automatic-kobo-and-kindle-ebook-arbitrage/) using their price match policy. I wasn't even aware of the price match policy and I've been using a Kobo for years (my first and only eReader). Anyone who enjoys reading and wants eBooks could benefit from [shopping at places that let you own your books](/articles/2025/dont-buy-new-ereader/). Kobo does have DRM, but as Terence says in his blog post, the DRM is easy to break. Remember, don't give money to companies that don't respect you enough to let you own what you paid for.

Alex talks about how she [created static Mastodon embeds](https://alexwlchan.net/2025/good-embedded-toots/) on her website. Rather than actually embedding the post it creates local HTML. This means even if the post eventually goes down the quote will still be on her website. It is amazing that people still embed content they have no control over and allow 3rd party websites to slow down their pages. HTML has a quote tag and if you really want your post to look like an embed you can do what Alex has done. It is always awesome seeing people create things that make the web a little better for their website visitors.

Nate talks about how [Blue Systems employees have transferred over to his new company Techpaladin Software](https://pointieststick.com/2025/03/10/personal-and-professional-updates-announcing-techpaladin-software/). They are still working on KDE and inherited Blue Systems' Valve contract for the SteamDeck. Nate and Blue Systems as a whole have been major contributors to KDE so hopefully that legacy continues under his new company. 

Lisa Herzog talked about the [ethics with accepting private money in academia](https://crookedtimber.org/2025/03/12/the-ethics-of-collaborations-between-academia-and-commercial-parties/). With public money drying up and active hostility towards academics in general growing it is hard not to accept funding from any source to further research. There is also the problem that research and researchers are often judged by the amount of funding they can secure. It is a complex topic that I am underqualified to cover in depth, but it is worth looking into.

Veronica explains [how to use VimWiki](https://vkc.sh/vimwiki-101/) and why it works for her. She also did a [YouTube video on the subject](https://www.youtube.com/watch?v=RmEtH5FQs28) if that is more your thing. I'm slowly getting familiar with Vim, but it is not something I'm ready to go all in on yet. I also take personal notes mostly with pen and paper so don't think I'll be using VimWiki, but it is a cool project that seems to work for a lot of people.

Matthew Graybosch mentions [All Anti-Vaxxers Lie](https://starbreaker.org/grimoire/entries/all-antivaxxers-lie/index.html) and that is the truth. There is no excuse to avoid vaccinating yourself and your children if you can. They save lives, prevent terrible outbreaks of diseases, and generally make the world a safer place for all of us. By spereading anti-vax lies you are actively harming others. It is not about politics, it is about basic human decency. There are people out there who can't get vaccines and by avoiding them you are making it much more likely that those people will get sick. To put it another way, anti-vaxxers are harbingers of death and deserve to be treated as such.

Wouter published a [wonderful overview of the Game Boy Advance](https://brainbaking.com/post/2025/03/an-ode-to-the-game-boy-advance/). It is an amazing console and likely one I will revisit one day. My mom got a GBA SP when I was young. I dismissed it as something not so great when I saw its pixel graphics compared to the GameCube and Xbox at first. My mom and sisters would play *Rugrats: I Gotta Go Party* (a minigame collection with a Rugrats theme) and one other game for it that didn't really appeal to me. My shallow mind didn't think there was much else to the system. One Christmas day I got a copy of Pokémon Emerald though, and that changed my entire perspective of the device. I never played a game so open before, I think it was the first RPG I played as well. 

### Videos

Justin Davies from justinthetrees made [sassafras flavored ice cream](https://www.youtube.com/watch?v=1DmGDGgxtHg). Root bear is my favorite flavor of soda, so this is something I'd love to try one day.

Robert from Ideal Idea showcases how he [used 3D printing to improve his work area](https://www.youtube.com/watch?v=gMAh_ZKRNnQ). I really need to pick up more CAD skills sometime in the future. He has some fun ideas.

Patty Gurdy released an album recently and has been uploading the complete songs to her YouTube channel. One of my favorite I've heard so far is her duet with Magga Einarsdóttir, [Álfarann](https://www.youtube.com/watch?v=eCKHf2qo8y8). Magga Einarsdóttir and her worked on creating this song together and there is a [video about that as well](https://www.youtube.com/watch?v=fd-rJHa9Npo). I love folk music a lot, maybe I should recant my statement from last month about not going out of my way to listen to music.

Hannah Kosoff talks about the differences between [Conservative and Liberal urban planning in the United States](https://www.youtube.com/watch?v=8N86A1-tJ7g). She highlights how a lot of Republican policies contradicts their own desire for personal freedom, autonomy, and local values. It always baffles me that someone who says they want personal freedom would want to remove transit options for themselves and others. I've heard people argue that making it easy for people to complete errands on foot and travel without a car somehow takes away freedom. Even drivers benefit from more transit options and walkable neighborhoods (for hopefully obvious reasons), but they will go out of their way to make sure sidewalks are smaller and highways are larger.

QuinnC's Videos created a [Raspberry Pi powered RoboSapien](https://www.youtube.com/watch?v=FOl8-dDiKfg) robot that gives the robot tracking, object detection, advanced movement, and more. I wanted a RoboSapien when I was a kid so it is cool to see people still playing around with them now.

Attoparsec created a [keyboard that has the 1000 most common English words](https://www.youtube.com/watch?v=wC-24QeoQu4) and some modifiers for applying inflected forms of said words. It is a really impressive and impractical project. 

Fraser Builds shows [how he fires his pottery](https://www.youtube.com/watch?v=UBW05kEA6Dc) over an open flame. A very calm video that is fun to watch. 

Snappiness shows off an [early Kodak Picture Maker kiosk](https://www.youtube.com/watch?v=BTkx8CamFbI&pp=0gcJCU8JAYcqIYzv). It is rather interesting to see and very cool that it is running on a Sun Spark system.

Niccolo Venerandi talks about why [BlueSky is not federated](https://www.youtube.com/watch?v=D0wbCctcEIA) in practice, why it is redundant with the existence of ActivityPub, and how we should be skeptical till BlueSky is actually federated. I don't really trust BlueSky either for many reasons. The Fediverse (ActivityPub) already serves the needs of people looking for a decentralized method of social media, BlueSky is just another corporate run platform that has yet to prove it won't be evil when VC funding dries up. I'm all for a diversity of options and there is an off chance that BlueSky will actually be good in the future, but it is very hard to trust it.

Niccolo Venerandi also talks about [Igalia, a worker owned tech co-op](https://www.youtube.com/watch?v=4wpqYR8L6m4). I'm a firm believer that co-ops are the closest thing you can get to a fair and equitable business under capitalism. It is nice to see Igalia improving open source while also giving employees what they deserve. More businesses need to be employee owned. In the west that scares a lot of people as they have been brainwashed against communism, but Marx was onto something with this whole worker owned means of production thing. I don't think communism is necessarily the answer, but capitalism certainly and demonstrably isn't.

GingerOfOz created [a working version of the Playstacean](https://www.youtube.com/watch?v=dSBNs3TeINc), a combination of a PlayStation and a crab. It is an awesome and humorous project that really makes me happy to see. I never had a playstation console, but I know there are a lot of great games for it. Everything truly does eventually evolve into a crab in the end.

Jeff vents about his frustration with buying [a new dishwasher only for it to require internet access](https://www.youtube.com/watch?v=5M_hmwBBPnc) to use all the features. Any product that requires the internet or an app to do what could have been done with a few buttons and a microcontroller is a product that shouldn't be purchased. I am not against progressive enhancement, but "smart" products targeting general consumers often need internet connections and all the problems that come with it. 

On a very concerning note, The Atlantic’s editor-in-chief, Jeffrey Goldberg, received a [signal group chat invite from Michael Waltz regarding a bombing on the Houthis in Yemen](https://www.youtube.com/watch?v=HFunw-2jKKc). This was not a hoax, but a real mistake as the chat was with some of Trump's officials planning the bombing. Under any other administration this would be surprising, but honestly Trump's team has never inspired faith. Signal is great, but it is not a place to be having classified discussions. They should have double-checked to make sure only the people who should be on the chat are present. This is disappointing and unfortunately expected behavior. Normally these people would all be fired and see time in prison, but I have doubts that proper punishment will be dealt to these people. Jeffrey Goldberg took a risk revealing this to the public, but performed a great service in bringing it to light. 

Gala Studio goes over how they [made their new home office](https://www.youtube.com/watch?v=nBxT9QFSBro). I have no eye for design, but it is interesting seeing how designers tackle problems.

Morley Kert [built a writing desk with a paludarium](https://www.youtube.com/watch?v=r52ooBsGr8M). This is something my sister would likely enjoy doing. A really fun looking project. 

## Onto Month Four

So much has already happened this year, but we still have a lot a head of us. There are amazing things all around us, great people to be with, and interesting things to learn. April will likely be a busy month for me, but I want to refocus on studying and learning. Look forward to more posts in the future.
