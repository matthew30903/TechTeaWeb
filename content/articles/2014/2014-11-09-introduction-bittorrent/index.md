---
author: Matthew
categories:
- Introduction to Computers
- Tech Tips
date: "2014-11-09T22:13:24Z"
tags:
- Bittorrent
- Cross-Platform
- Free Software
- Linux
- Mac
- Open Source
- Torrent
- Windows
title: Introduction to BitTorrent
aliases:
  - /introduction-bittorrent/
slug: /introduction-bittorrent/
---

BitTorrent has been around for many years now, since 2001, yet there are many who still do not know what it is or how to use it. Today we will lock at the basics of what BitTorrent is and how to use it.

What is BitTorrent?

To put it simply, BitTorrent is a way to download large files quickly and efficiently. BitTorrent itself is a protocol that handles the transferring of files across the internet. The major difference between BitTorrent and standard direct downloads is that when downloading through BitTorrent downloads from many sources at once whereas direct downloads come from one server.

Using this “swarm” of computers allows for faster download speed as you get little pieces of the file from many users who already have that file. The only server involved is a Torrent Tracker that keeps track of the file. All other actions are performed peer-to-peer (P2P) within the swarm. BitTorrent uses a system where you receive data from the “swarm” in exchange you become a member of that swarm to help send files that you have to others. This is known as Seeding.

Carmen Carmack from [HowStuffWorks.com](http://www.howstuffworks.com/) gives a general rundown of the process:


{{< figure src="./img/Torrent_Example.jpg" alt="Image: Traditional Download vs. Torrent">}}

> *   You open a Web page and click on a link for the file you want.
> *   BitTorrent client software communicates with a **tracker** to find other computers running BitTorrent that have the complete file (**seed** computers) and those with a portion of the file (peers that are usually in the process of downloading the file).
> *   The tracker identifies the **swarm**, which is the connected computers that have all of or a portion of the file and are in the process of sending or receiving it.
> *   The tracker helps the client software trade pieces of the file you want with other computers in the swarm. Your computer receives multiple pieces of the file simultaneously.
> *   If you continue to run the BitTorrent client software after your download is complete, others can receive .torrent files from your computer; your future download rates improve because you are ranked higher in the "tit-for-tat" system."

BitTorrent is only the protocol used to download the files, you will need specialized software to actually download the file, this is known as a BitTorrent client. The client handles all download operations on your computer. There are many client programs available for free, but for this example we will be using Deluge as it is open-source, cross-platform, and easy to use. If you are on a Linux system your distribution probably already comes with Transmission or Ktorrent which are both grate options)

First you will need to go to the Deluge [website here.](http://deluge-torrent.org/ "deluge")

Once it is done downloading and installing start it up. You should see something like this:

{{< figure src="./img/Deluge.png" alt="Image: Deluge User Interface">}}

As you can see it is a fairly straightforward interface. You have a traditional menu at the top as well as a tool bar that allows to add, delineate, pause, start, move up and down torrents in the queue, and open up the Preferences panel. The left most panel gives an overview of all torrent and tracker activity. On the right there is a panel that shoes all torrents and allows you to click on them to view more information in the bottom panel. On the bottom is all of the data about the selected torrent. Here you can see how much of the torrent you have, what files you have downloaded, how many peers are connected and how much of the file they have, and options that are specific to the individual torrent. We will go through each of these in depth later, but first we will need a Torrent file to download.

You can use any torrent file you wish, but for this example we will be downloading the Debian live CD. For this example we will be using the amd64 CD release. Debian is a Linux Distribution that is completely legal to download. You can get it [here.](https://www.debian.org/CD/torrent-cd/ "debian")

{{< figure src="./img/Deluge_Download.png" alt="Image: Deluge Download User Interface">}}

You should be able to open the file in Deluge right from the browser so there is no reason to save the file. This file is information that Deluge needs to download the Debian ISO image, not the ISO itself. Once it opens in Deluge you should see a screen similar to the image on the right.

This screen gives a general overview of the torrent file including its name and the files that are included in this file. Under the options tab you can select the location you wish to download the file and set bandwidth limits(we will go over this later), but for now we can just select the add button to start the torrent.

We will go over the basic options and panels in depth in the next post.

Source:

Carmack, Carmen. "How BitTorrent Works" 26 March 2005. HowStuffWorks.com. (http://computer.howstuffworks.com/bittorrent.htm) 08 November 2014.