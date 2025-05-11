---
authors: 
- "Matthew Lamont"
categories:
- Game Development
- RPG Maker MV
date: "2018-03-20T14:26:15Z"
guid: https://www.blog.mattlamont.com/?p=484
id: 484
tags:
- RPG Maker MV
- Game Dev
- Tutorials
title: Let's Make a Video Game | RPG Maker MV
aliases:
  - /make-video-game-rpg-maker-mv/
series: "Make a Game with RPG Maker MV"
slug: /make-video-game-rpg-maker-mv/
---

Many people dream of making a video game. Gaming is one the the ages most popular hobbies and stories of people getting rich off side projects are everywhere. The truth is very few people actually want to make a game nor are the success stories nearly as common as we would like to believe. Building a video game on your own is a massive undertaking and rarely yields success financially. That said, there are options. Over the next few articles we will explore building a small video game in RPG Maker MV.

## Getting Started

After deciding we have the determination to make a video game we need to do several things:

1.  Define our goal
2.  Pick a genre
3.  Pick an engine
4.  Refine our concepts
5.  Estimate costs
6.  Build our team

Many are tempted to run ahead and make things up as they go. That rarely works. If you look on Steam or Itch you will see many unfinished projects. These 'games' are unpolished, poorly written, and use the generic features of what ever engine the developer could find at the time. To avoid this we need to define our goals beforehand.

## Define out goal

Before we begin building our game we need to know the scope of our project, the story, the type of game we wish to make, etc. We need to set expectations and do research around the market we are targeting.

### Write our Synopsis

First we will get a general idea of what our story will be about. Some video games are more about the mechanics and some about the world they inhabit, but most start with a story the developer wishes to tell. For this reason we will focus first on a story and then build a world and mechanics that fit that story.

> Lets say we want a game following a band of mercenaries who are about to be dragged into a war between two rival nations.

### Pick a medium

Would this story play out best as a platformer? Perhaps a shooter? A grand strategy game? The genre we chose will greatly impact the rest of the decisions we make in development. The engine we use, the mechanics we design, and the way we flesh out our story all depend on how the game is played. An action game is going to have fewer cutseens and less dialogue than a RPG or Visual Novel. A RPG will be far more time consuming and costly to develop than a platformer.

> With that in mind we will say that this will be a role playing game centered around one particular mercenary who is having second thoughts about the war.

### Define our scope

Now we need to decide the scope. Are we building a 100 hour epic or perhaps a 15 minute tech demo? Do we want to show this to our friends and family, release it to the public for free, or perhaps make our millions from Steam and GOG sells? These questions will help us decide how we want to write our story and how we go about marketing it. If we decide to sell our video game it will need a lot more refinement than if we just gave it to a friend for a birthday present.

You must have a realistic goal for your first game, many developers set impossible goals and give up under the pressure. We will be in a difficult position if we are to build a game 100 hour dream game in between work and taking care of the family for example.

> Let’s imagine we are working full-time with no other responsibilities. After work each day we will dedicate an hour to game development. Our goal is to build a 1 hour long episodic 2D RPG telling the story of a mercenary as he fights through a war.

## Pick an Engine

Now that we know our story and what type of game we wish to make we need to decide on an engine. A game engine is a prebuilt set of libraries and tools that we can use to build our game. These range from a few python libraries to full development environments. There are far too many to count and you will have to do your own research to find the best one for your needs.

In our case we chose to build a 2D RPG so we will pick an engine that has great 2D support and provides us the tools to build an RPG. We have limited amount of development time and few resources. This brings us down to two engines that work well for our project.

### [Godot](https://godotengine.org/)

{{< figure src="./img/make_game_godot_animation_editor" alt="Image: Godot Animation Editor">}}

Godot is a free and open source (MIT) general purpose game engine for both 2D and 3D games. It has support for all major platforms (Linux, Mac, Android, Windows, FreeBSD, OpenBSD and Haiku and iOS) and multiple programming languages. The catch is that you will have to build most of your resources from scratch. Godot does some of the heavy lifting, but you will have to write the scripts and make the artwork yourself. Godot is not ready to make a RPG out of the box, but it is powerful enough to do so.

### [RPG Maker MV](http://www.rpgmakerweb.com/products/programs/rpg-maker-mv)

{{< figure src="./img/make_game_rmmv_map_editor" alt="Image: RPG Maker Map Editor">}}

The latest release in the RPG Maker series of engines, RPG Maker MV is a proprietary engine that supports all major platforms and utilizes JavaScript and HTML5 for programming. The engine is easier to use than Godot and is built for our particular task. All the functions for a RPG already exist and it comes with many resources prebuilt for our use. The catch is that it is proprietary, not as flexible without putting in effort, and costs money. That said there is no royalty fees and you are getting a lot of resources with it.

<blockquote>Due to the cost of hiring artists and scripting we will use RPG Maker MV for this. It does cost more initially, but we can get away with using the default assets till we are ready to publish our game.

## Estimate Costs

We have made it to the final stages of planning out our game. We now need to estimate how much this project will cost us. If we are going to do this by ourselves or with friends who are willing to donate their time and skill, the costs will be that of the engine and the time we put in. If we need to hire a programmer for a specialized system or voice actors, however, we will be needing a much larger budget.

We need break down our costs
> $80.00 – Engine
>
> $25.00 – Main Character Portrait
>
> $150.00 – Tileset
>
> $300.00 – Title Theme Music
>
> Etc.

## Refine our Concept

Now that we have our video game planned out we need to actually flesh out our story, gameplay, and other plans. We need to build a detailed game design document that explains the setting, characters, story, and gameplay. How is combat going to work? What abilities does the main character have? How does our key mechanic play into a particular level? All these things will be important to the development of our game.

Our RPG’s game design document may start something like this:

> [Insert Title] is a turn-based RPG that follows a mercenary during a great war. Combat is the focus, with each character having unique abilities that will change the outcome of battle. Each level of the game takes place as an episode during the war and consists of self-contained goals. After completing a level, the player will be awarded a grade and rewards based on performance. These will aid the player in the next level.


It is a bit rough, but it will do for a start.

Next time we will start exploring the RPG Maker engine and design the first level of our video game.