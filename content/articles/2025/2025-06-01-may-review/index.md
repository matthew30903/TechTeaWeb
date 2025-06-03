---
title: "May 2025 Review"
date: 2025-06-01T09:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Monthly Favorites
  - Monthly Review
slug: /may-review/
keywords:
  - Review
description: A lot has happened this month. Lets go over what has been going on in my world and share some fun links. 
---

It has been another busy month, but not much to really report in my personal life. A majority of this month has been spent reading, playing video games, playing around with my own video game projects, and drinking tea. Work has been busy as well.

There is a lot going on in the world right now and sometimes we just need a break. I focused on hobbies and tried not to focus too much on what is outside my control. 

<!-- Project 2025 is still being pushed in full force in the United States, surprising no one. It is terrifying to know that the U.S. is taking away worker's rights, defunding scientific research, denying the environmental destruction caused by pro-republican businesses, and increased taxes on the poor while lining the wallets of the rich (via tariffs). That is not to mention the outright hostility towards anyone not rich, white, and biologically male. He even put an anti-vaxer in charge of medial and food regulation. 

Trump has threatened states, private and public agencies that oppose him, and even individuals, he has then sent his followers to enact his punishments against them, just look at what he did to Maine. Is it illegal? Yes. Is it unconstitutional? Yes. Did that stop them? No. Will it stop them in the future? As things stand now, most likely no.   

If you tell me you voted for Trump and are surprised by anything he has done so far I won't believe you. He said he was going to do all this, his cronies wrote project 2025, and he was already doing some of this last time he was in office. Either you are lying to me or you are so willfully unaware that you may as well be. I'd be glad if you don't support him now, but you need to do some soul-searching. Only evil could stand with an organization as vial as the current federal Republican Party or Trump and his cronies.    -->

One of the bigger things I've been playing around with has been making a game in RPG Maker MZ. The game engine is fairly easy to use, but powerful enough to do some rather amazing things if you are creative. I don't think I'll release a game for a while, if ever, but RPG Maker is a great tool for stretching your creative muscles. My little brother is also working on a project in the engine so it is fun creating small scripts and event systems to solve his problems. Learning more JS doing this than I did working on this website or in college. 

## Games

Mostly been playing *Xenoblade Chronicles X* on the Switch this month. The game is fun, though it has some problems with how grindy some of the quests can get. The game expects you to learn the mechanics and exploit them if you want to have a fun time. I'm only just finished Chapter 4 so I'm fairly early into it, but I can already feel it ramping up into something good. Characters and exploration is where this game is at its best, it is very anime, but not like *Xenoblade Chronicles 2* was, more in the way you expect a more mature RPG to feel.

I've got way too many more games to play this year, but I'll stick with Xenoblade for a while longer.

## Movies

### Poor Things

I watched [Poor Things](https://en.wikipedia.org/wiki/Poor_Things_(film)) with my girlfriend, this one is not for kids. I have mixed feelings on this one. A doctor puts the brain of a baby into the body of its deceased mother and raises her as his own, naming her Bella Baxter. Bella starts off with an infant mind and grows over the course of the movie. She starts to discover her sexuality and that becomes a core focus of the movie. I think I understand why the writer and director went the direction they did, but this movie's depiction of the 'sexy born yesterday' trope makes things more than a little awkward. Even though I find it awkward I do think they depicted Bella's growth, development of personal agency, and sexual liberation with respect for the subject mater. It felt a little forced and rushed at moments. There was an excessive amount of sex scenes.

The art direction, cinematography, and general depiction of the world the characters inhabit is well done. There were a few places where the ultrawide angle shots were disorientating, but I think that fits the overall feel of the movie.  

While I do have some issues with it, the movie was fairly good. My girlfriend enjoyed it for the most part, but generally agreed with my criticisms. We will probably need to rewatch it in the future to get a better grasp of our feelings towards the movie. 

## Books

### Witch Hat Atelier by Kamome Shirahama

I normally avoid recommending anime and manga here due to how a lot of it can go against western sensibilities, but Witch Hat Atelier has been an amazing series since I started reading it a year or so ago.

The story follows Coco, someone who always dreamed of being a witch. She was told that she couldn't be one because magic is hereditary. I won't spoil too much, but it turns out that it was a lie and anyone can use magic if they know how. When she learns that she starts practicing magic in secret, resulting in tragedy. She becomes the apprentice to a witch in order to fix things. 

The story centers around Coco's journey as she and the people she meets are constantly put into conflict with societal rules put in place to keep people from abusing magic. My writing can't give this series justice, but it is well worth a read. It poses great moral and philosophical dilemmas for the characters, has an amazing and visual magic system, and artwork that fully takes advantage of the medium. 

The series is still publishing, but if it continues as strong as it has been going so far it is likely to be one of my favorite fantasy series. 

### The Linux Command Line by William Shotts

I'm not very far into this one, spent the month mostly reading a bunch of novels and catching up on Witch Hat, but what I've read so far is great. Shotts clearly has passion for computers and wants people to find the same joy he has when using the terminal. It isn't a scripting book or a sysadmin book, but more of a guide on how to really know your computer. Love it so far, No Starch Press always seems to publish great technical books.

## Links:

### Cool Projects

[Yazi](https://yazi-rs.github.io) is a TUI file manager. I've been doing more in the terminal lately and wanted to try out a terminal file manager. Yazi is fast, seems fairly customizable, and works out of the box without configuration. Dolphin is my main file manager as a KDE user, it is the best file manager I've used on Linux, but it is cool to see how other tools work and being able to do so much in the terminal is a huge plus for terminal based workflows. Yazi doesn't really do anything that can't be done with the standard Unix tools, but it gives you a lovely UI to interact with them. 

[Phockup](https://github.com/ivandokov/phockup) (short for photo backup, a very unfortunate name) is a nifty little script that sorts photos into subdirectories based on their metadata. I was using Nextcloud for my photo backup and it automatically did this for me, but I've not used it since nuking my server. Now I'm using a dedicated camera and Syncthing on my phone, due to that all my photos end up in one folder. I do plan to eventually write my own script for this task, but currently Phockup does a great job at what I need it to do and it's available in Nix. Currently, I have syncthing setup to send photos to a folder that Phockup is set to sort. I'm using a systemd timer to check the folder as I was having issues using ionotify to watch the folder. If anyone has ideas to better automate this let me know.

### Music

Dave Eddy released an album with some awesome instrumental pieces, [*Nightfall*](https://nightfall.ysap.sh). You can curl it into bash to get an awesome TUI interface for listening to it. You will need `ffmpeg` and `curl` to get it working, but most systems already have them installed. **Always vet code before you open it in bash, generally it is a bad idea to curl into bash in general for security reasons.** That said, here is the command to listen to it in the terminal:

`bash <(curl nightfall.ysap.sh)`

He also has a [YouTube channel](https://www.youtube.com/@yousuckatprogramming/videos) where he talks about sysadmin, programming, and UNIX stuff. He has a [video going over how he created the music player script](https://www.youtube.com/watch?v=J4iUQiZrj98).

### Articles

I don't see a name on this website, so I'm going by the site's title fireborn. Fireborn talks about how [accessibility on Linux is a nightmare](https://fireborn.mataroa.blog/blog/i-want-to-love-linux-it-doesnt-love-me-back-post-1-built-for-control-but-not-for-people/). Software is constantly getting more complex, tools that used to work are no longer maintained, and distros don't ship with the accessibility tools that do work. People without sight are some of the most inconvenienced people when it comes to computers, many developers don't know what is accessible if they care at all, our apps are complex and made for those who can see, etc. Fireborn loves linux and hopes for it to get better, but it just ins't there yet. I try my best to at least make this website accessible, but I'm not blind nor am I a skilled developer. Even the most skilled of developers have trouble creating tools they won't use and unfortunately the Linux desktop is built by more people with sight than without. I've seen KDE and many other organizations put more focus on accessibility the last few years, hope it will be enough and fast enough for all to enjoy the freedom that comes with Linux. 

Michał Sapka talks about [how FOSS software works as an extension of himself instead of a replacement](https://michal.sapka.pl/2025/repositioning-tech-in-my-life/). Many proprietary programs try to automate their users' behavior, remove friction to the point of brainrot, and use dark patterns to addict users. Free software doesn't have the profit motive to do such things. This inherently makes it less popular, but it also makes it infinitely more useful and enjoyable. 

Carl Svensson shares the [design languages and styles of old desktop icons](https://www.datagubbe.se/icons/) from different systems. A lot was lost in the transition from interesting and expressive icons to the more corporate icons of today. Fortunately there are creative people out there making icon themes. 

Benj Edwards believes we need to [regulate capitalisms' worst tendencies](https://www.vintagecomputing.com/index.php/archives/3292) if we wish to have freedom and control over our devices. I'm a big fan of open source, self-hosting, and being a conscious consumer, but not everyone is technically inclined. We need regulation to put a leash on corporations and the extremely wealthy in order to spread freedom, privacy, and personal control to everyone. 

Olivier Lambert from Vates runs through all [the open source software they use to run their business](https://vates.tech/blog/the-open-source-we-use-at-vates-2025-edition/). It is lovely seeing an open source company using open source software to run their business. I hope this encourages other businesses to embrace more open software for their infrastructure. 

Keven wrote a [guide for how to think deeply](https://cliophate.wtf/how-to-think). Most of this is common sense for anyone coming from a more philosophical, academic, or more self-agency focused background, but schools have really dropped the ball regarding critical thinking skills. I like how Keven thoughtfully broke down how he sees thinking. I do completely disagree with the idea that current generative AI models are useful tools in comparison to almost anything else, but otherwise I agree with him.  

Leilukin switched from [VS Code to Neovim recently](https://leilukin.com/blog/posts/2025-04-03-i-use-neovim-btw/). I've been meaning to switch from VSCodium to Neovim myself as I'm trying to dive more into a terminal based workflow. Congrats to them and I hope to read more about their switch in the future.

At the start of the year Adriaan De Groot's [bank app stopped working on their phone, essentially making their phone e-waste](https://euroquis.nl/blabla/2025/01/27/e-waste.html). The app stopped working on older versions of android and unfortunately their current phone runs an unsupported version. While I'd avoid any bank that requires a mobile app for basic function, that doesn't seem to be an option for Dutch banks. There are likely legal compliance reasons at play, but it is not an ideal situation. 

Matt talks about how the [web is more than the corporate net many of us see all over the place](https://fyr.io/post/world_wild_web). It is full of small websites made by humans like the ones I share in these links. The web needs more of these small websites and Matt invites all of us to create more.

Wouter gives a little insight into [his world of clutter](https://brainbaking.com/post/2025/05/junk-contemplations/). Having hobbies that involve collecting, having pets, and having a young child all add up and make it very hard to keep things clean and organized. That was the way it was with my family growing up, and I'm sure no matter what Wouter does it will always build back up. I'm doing much better than I used to due to my stringent budgeting this year, but it is really easy to accumulate way too much stuff even without a kid. 

Annie gives a helpful little reminder that there is [no such thing as a neutral stance when it comes to human rights](https://anniemueller.com/posts/a-neutral-stance-is-for-weightlifting-not-for-human-rights). You can't be neutral when someone says "x group doesn't deserve to exist" or "those people shouldn't have access to that medical procedure because I don't agree with it". Either you are for protecting people's rights or you are complacent in allowing those rights be denied to others. There is no possible middle ground. 

Xandra shares her personal thoughts on [how to run a community](https://library.xandra.cc/moderation/). I rarely post on forums or other online community pages, but generally I agree with what Xandra is saying. If you want a community to thrive you have to express shared values and protect them. Even free speech absolutists need to have a community guideline stating that, else they will find themselves surrounded with people they would rather not be. Even if a group is composed of virtuous and like-minded individuals needs guidelines because not everyone will agree on everything. I do dislike codes of conduct that are overly complex, wordy, or exclusionary due to poor word choice (something that was very prominent in many early codes of conduct for software projects), but that doesn't mean having no rules is the answer. It is the rules that help set the tone and feel of everything that follows. 

Dylan Beattie gives some thoughts on the [difference between programming and turning that code into an actual product](https://dylanbeattie.net/2025/04/11/the-problem-with-vibe-coding.html). Creating a little script for personal use (programming) can be fairly easy and doesn't need as much specialized knowledge, but the moment you want to sell it or scale it out to other users the amount of things to consider grows exponentially. While I don't think externalizing the thinking and understanding of code to an unthinking AI is coding, I certainly know it is not a way to create a product.  

### Videos

Design Theory talks about why it is [hard to design and build around right to repair](https://www.youtube.com/watch?v=nrv45bvP8qo) and the social, political, and economic changes that need to happen to get more repair friendly products to market. 

Kafryn D talks about [her experience in a cult, how to identify one, and how to get out](https://www.youtube.com/watch?v=VaSAesX3it4). Never been in a cult, but there were many times when someone would try to recruit me for one. Stay vigilant, especially when you are feeling down. Cults pray on those who need help the most.

Cinzia DuBois discusses the [joys and importance of close reading outside of academia](https://www.youtube.com/watch?v=k0zx4-20Jz0). Truly interfacing with a text is mentally taxing, but worth so much. It is sad that many people don't read deeply, if at all. Hopefully this video will encourage some to read deeply. Then again, if you are reading my random links and comments you are probably the type of person who gets caught up in deep rabbit holes.

Liz Dye from Legal Eagle talks about how [Trump has been dutifully implemented the recommendations in Project 2025](https://www.youtube.com/watch?v=5jyw3NE-SAs). If you want details on how the United States is being dismantled from within or just something to be depressed about, this video does a good job at summarizing the situation.

CHWTT showcases how he made a [rack mounted macro pad](https://www.youtube.com/watch?v=_hcOAzanCvQ). This is something that would be awesome to have. I did look at a streameck in the past and they are really cool, but very expensive for what they are. I look forward to seeing if this project develops further in the future. 

okooptics [made a 1 pixel camera that can take low resolution photos of objects](https://www.youtube.com/watch?v=EE9AETSoPHw). It is really amazing what one can do with such limited optics and knowledge of how they work.

Ana Fern tries to explain the [right wing 'masculinity' obsession with eating raw animal products](https://www.youtube.com/watch?v=FnQiUE-gg4g). Ana talks about how their extreme fad diets, with a focus on the carnivore diet; how it is anti-globalist, anti-feminist, and anti-multiculturalism and how it is fueled by fear and distrust. Controlling how people eat is another tool extreme groups use to control and distinguish their followers. I probably don't need to tell you how backwards and sad the online 'masculinity' movement is. It is a parody of everything that is virtuous or masculine, but people don't fall into such an ideology without a reason and I think Ana tries to understand the reasoning of these backwards ideas with respect.

Asad Anum thought he didn't like RPGs, but found out what he really didn't like was [games that are ashamed of their own mechanics](https://www.youtube.com/watch?v=ny6dhZHzw0U). A lot of media in general is like this nowadays. Due to the numbers go up addiction of shareholders, game developers are incentivized to smooth over all friction. As with all things, friction is where we grow, develop skills, use our brains, and find joy. That is not to say we enjoy friction for its own sake. A lot of products, games included, become frustrating due to their overwhelming bias against friction. This means taking away complexity that people can enjoy, removing or hiding tools that allow you to do more than the basics (look at GNOME and Android), and overall remove the incentive to get invested in anything. Games and products that respect their users are getting rarer, but it is all the more reason to seek them out.

Dmytro Engineering shares how he [reverse engineered a shady android thermal camera to get it working on his computer as a webcam](https://www.youtube.com/watch?v=bePf-qhZ_Vg). He is doing good work open sourcing solutions that help these devices go from potentially privacy invasive e-waste into something truly useful. If hardware requires an app on your phone that needs location, phone logs, and more, it is probably not worth whatever price you paid for that hardware. That said, there are so many amazing people trying to make the world a better place by hacking these devices and releasing their findings for everyone.

Bread [explains the basics of SSH](https://www.youtube.com/watch?v=WwGRGfLy6q8) in a simple way. If you've managed more than one computer at a time, checked out code from a git repo, or run a server or two you are probably at least somewhat aware of SSH and how to use it. Bread explains a little more than just how to remote into a system, covering basic security, logging in with SSH keys, and a little more. I feel like it is such an essential tool and Bread explained it in an easy-to-understand way. Her channel is full of good to know Linux knowhow, give it a look. 


Recording retro game consoles isn't easy, but Jon from GVG needs to do it to create videos for a YouTube channel. He [goes over his recording setup](https://www.youtube.com/watch?v=XroabpwQc5M), including all the devices he uses to capture game footage. Really cool stuff that might be useful for any aspiring videographer wanting to make video game videos.

## Another Month Gone By

I've not been very active on here this month. I've kinda been neglecting a lot of things in the tech world lately, life has gotten busy.

I do want to get back into posting about tea and tech. I've taken a few good photos so I might spin up a gallery page soon like I keep saying I will.

I also got a Mudita Kompakt to replace my Pixel 3a, might write a review or impressions post about it sometime in the next few months after getting used to it and its limitations. There was a draft post on my perfect phone and three of the requirements were that it was small, had an eink screen, and it ran a degoogled android. This phone does those things, but also has some problems.  

Please let me know if there is anything you would like me to talk about in a blog post. I want to write more about using computers to tackle real world problems.
