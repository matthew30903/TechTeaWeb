---
authors: 
- "Matthew Lamont"
categories:
- Game Development
- RPG Maker MV
date: "2019-01-01T12:00:29Z"
tags:
- Game Design
- RPG MakerMV
- Tutorials
- Video Games
title: RPG Maker Events | RPG Maker MV
aliases:
  - /rpg-maker-events-rpg-maker-mv/
series: "Make a Game with RPG Maker MV"
slug: /rpg-maker-events-rpg-maker-mv/
---


Last time [we explored the map making interface](https://www.blog.mattlamont.com/creating-rpg-maker-project/) and made our first map in RPG Maker. It looks nice, but there is not much for the player to do.

{{< figure src="./img/RPGMakerTutorialIntro3.png" alt="Image: RPG Maker Map">}}

## Enter Events

Events are a collection of commands that happen under certain conditions. Think of these like mini-programs. A shop keeper is an event, a map change is an event, even battles can be triggered by events.

To get started we need to enter Event Mode(F6) before we can start adding events. A grid should appear showing you the dividing lines of each tile. Right click anywhere on the map and you will see a context menu with many options for events. Click new and the event editor will open up.

## The Event Editor

{{< figure src="./img/RPGEvent1NewEventWindow.png" alt="Image: RPG Maker New Event Window">}}

There is a lot going on here, but fortunately RPG Maker splits the window into easy to understand parts.

### Title Bar

In the title bar we have the event ID, this is the number that will get referenced by other events and scripts we write in the future.

### Name and Page Controls

Then we have the event name, this is for your reference and will not be seen by the player.

Notes are similar to the name in that they are for your reference, but some plugins use them for special commands.

Next we have page editing features. Events are broken up into pages. Most events we will work with will only have one or two pages, but you can have up to 20 different pages. You can see that all sections underneath this part of the interface are in a tab, this is an event page.

### Page Conditions

This is where event pages come in handy. We will explain this stuff in detail in a later article, but events that have unmet conditions will not execute. Each page can have a condition. Lets say we want something to happen only once or the dialogue of a character changes each time we talk to them, this is where you can make that happen.

### Image

{{< figure src="./img/RPGEvent2_EventImage.png" alt="Image: RPG Maker New Event Window">}}

Events are invisible to the player by default, but we can give them a character image. These images can be doors, switches, animals, monsters, or anything else that you would like your player to interact with. Each character image is split into cells. These cells are three by four. This makes an animated character sprite. The first image is the right foot, then standing still, and finally the left foot. The process repeats downwards for each direction. These characters are placed on a sheet of 8 characters.

Images are a bit complex and we will cover them in-depth at a later date.

### Autonomous Movement 

Movement is another complex feature that could use an article of its own. With autonomous movement you can make a sprite move without any input from the player. This can be random, always moving towards the player(Approach), or defined by you(Custom). Speed is how fast the sprite moves and frequency is how often.

We will be working a lot with movement in the future, but it is okay to set this one to fixed for now.

### Options

Options determine how the event will be displayed.

Walking displays animation when moving, this is what we want to use for most of our characters.

Stepping displays the stepping animation while the character is stopped. This makes fire and lights glow automatically. This can also make a character walk in place.

Direction Fix prevents the direction that the image is facing from changing while moving.

Through allows to pass through terrain and events that cannot be passed through.

### Priority

Priority determines how the event will interact with the player and others.

Below characters will let players and so on will be able to move on top of this event.

Same as characters will be at the same height as characters, and it will not be possible to go through this event.

Above characters players and so on will be able to move beneath this event.

### Triggers

Triggers determine how the event activates.

Action Button activates the event when the player is touching the event and presses the action button. This is how events are handled by default.

Player Touch activates when the player touches the event. You could use this for things like pressure plates. 

Event Touch activates when an event makes contact with a player through either their autonomous movement or the player touching them.

Autorun activates as soon as event conditions are met. This is useful for introduction sequences and one time events that must trigger no mater what.

Parallel activates the same way as autorun, but the it runs in the background. This lets the player move and continue playing even as the event is executing. This is great for background elements that need to happen, but should not interrupt gameplay.

Warning: Autorun and parallel can cause your game to enter an endless loop if you do not stop it. Always end your autorunning events with something that stops them from running.

{{< figure src="./img/RPGEvent3_EventCommands.png" alt="Image: RPG Maker Event Commands">}}

### Event Contents

The right side of the event editor contains all the event commands. This is where the magic happens. Today we will only cover a few commands, but these will be the building blocks for more complex systems in the future.

Double click in the contents section to open up a list of event commands. There are a lot of them, but they are broken up into easy to digest Groups.

We are going to start with the Show Text command. This will let us make a dialogue box that the player will see when they activate the event. We can chose a face image to show along with the text. You can change the background and position if you wish. For this example we will have the character say "Hi, how are you?"

{{< figure src="./img/RPGEvent4_TextCommand.png" alt="Image: RPG Maker Text Command">}}

Now that we have a question we should let the player respond. We will use the Show Choices command to do so. This will let the player make a choice, we can execute different commands based on their response.

Lets say "Good" and "Terrible" are our choices. When we enter the command you will see that there is text that says "When good", "When Terrible", and "End". Every command we place in the Good section will only execute when the player selects "Good" and the terrible section only executes if "Terrible" is selected. Everything entered after the End statement will execute no matter what.

Lets make our event respond to the player's choice. Afterwards our event should look something like this:

{{< figure src="./img/RPGEvent5_HowAreYou.png" alt="Image: RPG Maker Event Results">}}

Now we just need to play test the game. Give it a try and see your world come to life!

## Wrapping Up

RPG Maker has many more commands that we will cover in the future. You should read the documentation for more details in what each event command does.

We will start building our database and make more events in the next few tutorials. Look forward to it.
