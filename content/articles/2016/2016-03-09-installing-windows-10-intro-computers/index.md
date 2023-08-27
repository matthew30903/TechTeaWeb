---
authors: 
- "Matthew Lamont"
categories:
- Introduction to Computers
- Windows
date: "2016-03-09T10:53:36Z"
tags:
- Tutorials
- Windows
title: Installing Windows 10 | Introduction to Computers
aliases:
  - /installing-windows-10-intro-computers/
series: "Intro to Computers"
slug: /installing-windows-10-intro-computers/
---

Last time we went over [computer hardware](https://www.blog.mattlamont.com/computer-hardware-introduction-computers). Today we will be installing Windows 10. Windows 10 is the most recent version of the Windows Operating system (OS). We will first go over installing the OS from a disk, if you bought a computer with Windows 10 on it you can skip ahead to part two.

{{< figure src="./img/00-Language-Select.png" alt="Windows 10's Localization Selection">}}

## Part 1: Installing from Disk

To interact with menus in windows you will use the **left mouse button** to select items and the **keyboard** to type information.

The first thing you will see when you start installing the system is the localization settings. You will want to select your language, time and currency format, and keyboard to mach your region. In the screen shot we have everything setup for a United States computer. Then hit Next.

On the next screen you should screen **Install now** and a **Repair your computer** button. Click **Install now**.

{{< figure src="./img/02-Enter-CD-Key.png" alt="02-Enter-CD-Key">}}


Windows will ask you for your serial number. It will be on the case of the installation disk. If you do not have it you can click **I don't have a product key**, but you will run into trouble later if you cannot find it.

The next window will ask if you want to **Upgrade** or do a **Custom install**. We want to do the second. Click **Custom**.

You will just need to click on your hard drive and then the next button on the next screen, unless you know what you are doing.

We will go over partitioning in a later article.

{{< figure src="./img/04-Installing-Windows.png" alt="Windows 10 is installing, it will only take a minute.">}}

The next window will show the installation progress of Windows 10. This will take a few minutes. After it is done your computer will restart.

## Part Two: Setting up Windows 10

Now we start setting up Windows 10 for use. This is where things get tricky for the uneducated user. Windows 10 will do everything in its power to get you to consent to giving more information than you should. If you do not care about your privacy you can ignore the next part of the article, but you should care. “but I have nothing to hide.” is an evil and dumb statement, never consent to giving your information when it is not required.

{{< figure src="./img/05-Express-vs-Customize.png" alt="Customize Install.">}}

The next screen will ask you if you want to **Use Express settings**, you do not want to. Each point that the installer makes about why you want to use them is another piece of your private life that Microsoft can use for marketing and something that can be used against you.

There is a small **Customize settings **button near the bottom left of the screen, click it.

The next few windows will have a lot of options you will want to click off.

{{< figure src="./img/06-Personalization.png" alt="Oh where art thou, oh where art thou privacy?">}}

You will want to click each one of these option to off. These options will allow Microsoft to track everything you type, your location, your calendar information, and the

contact information of others. Most of the programs that use these “features” are more prevalent on cellphones, so you do not benefit much by giving this information to Microsoft.

Once you have everything off click next.

### Connectivity and error reporting:

Computer security 101: Never connect to a network you trust, ever. The next three options are more dangerous to have on than just giving Microsoft your information. When you connect to a network you make your computer open to what is on it. You will want to change these to off.

Sending error reports to Microsoft actually sounds like a good idea, but in my experience diagnostics never return results. It is better not to give Microsoft this information as you will not see results and Microsoft will sell what they get from you.

### More options to turn off:

{{< figure src="./img/08-Browser-Protection-and-Updates.png" alt="More things to turn off, hooray!">}}

Windows 10's SmartScreen feature is useful if you go to less savory websites, but in exchange, Microsoft gets to know where you have been online and what you are downloading.

Page prediction will be useless for us as we will be using a third party program to brows the internet. If left on, Windows 10 will send your internet and download history to Microsoft. Even if you do use the integrated web browser, you will not benefit much by having this on.

The last option will use your computer to send updates to others and allow you to receive them from others. This will use your internet connection, thus wasting bandwidth and slowing down your internet.

Turn these off.

Windows will restart after you click next.

## Part Three: Creating a Local Account

We are almost done! Unfortunately Microsoft tries to ware on your willpower by making it easier to just hand over the keys to your life.

{{< figure src="./img/09-Sign-in-now.png" alt="It is a trap! Do not fall for it.">}}

Windows 10 will ask you to sign in to or make a Microsoft account. This account will allow you to connect your devices and will allow Microsoft to put a name, address, email, and phone number to all the data they collect.

They make it hard to say no by making the **Skip this step **and **Microsoft privacy statement **buttons small. Read that privacy statement, it is vague and misleading, but it basically states that Microsoft will be sharing your information with the government, sending it to advertisers, and using it for the improvement of Windows 10.

We will want to **Skip this **step. There are some honest benefits to using a Microsoft account, parental controls and online backups, but there are alternatives that do not want to sell you ever chance they get.

### Creating a Local Account

{{< figure src="./img/10-Create-an-account-for-this-PC.png">}}

We are going to setup the account for the first user on this computer, this will be the system administrator and will have full control over the system.

The user name can be your name or anything you want. On this system I will be using “Random Thoughts”. The password is very important. This is what keeps others out of your computer. It would be a shame to have gone through all that effort to lessen Microsoft's grip just to hand the keys over to someone else. Use the keyboard to enter one that **uses a combination of Upper and lower case letters, symbols, and numbers**. Unless you are expecting someone with physical access to your computer to brake into your computer, it does not need to be overly strong.

An example password could look something like this: hTF1%g%#Gl#6U

**Never use password as a password.**

The password hint can help you remember what you have entered here, if you forget your password you will not be able to access your computer.

Now Windows 10 will play an animation as it sets things up for the new user. Just wait wist it finishes.

{{< figure src="./img/11-We-are-done.png">}}

We are done, just one more thing to do.

Congratulations, Windows 10 is now installed. There is just one more step. If you have your computer connected to the internet already, you will want to decide if you want your computer viable to others on the network. If you are at home you can select yes. If you are using a laptop or a computer that is on a public network you will want to say no.

If you have no plans on running a server or doing anything regarding computers interacting with each other you are better off saying no, you can always change this option.

We will be going over the windows interface next time and setting things up for you to use. We will also install our first few programs in the next article.