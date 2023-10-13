---
title: Test Linux in a Virtual Machine
authors: 
- "Matthew Lamont"
date: 2022-02-03T11:32:16Z
draft: false
categories:
  - Linux
  - Tech Tips
featuredImage: ./img/linux_in_virtual_box_featured_image.png
tags:
  - FOSS
  - Linux
  - Open Source
  - Virtual Machine
  - Tutorials
slug: /test-linux-in-virtual-machine/
aliases:
  - /test-linux-in-virtual-machine/
keywords:
  - Virtual Machine
  - Linux
description: So you have decided to check out Linux. Today we are going to help make the process a little easier by installing a Linux distribution inside a Virtual Machine.
---

So you have decided to check out Linux. Maybe you are fed up with Windows or you are just curious. Regardless of your reasons you are probably overwhelmed with the options and the conflicting information you see online. Today we are going to help make the process a little easier by installing a Linux distribution inside a Virtual Machine (VM).

## What is a Virtual Machine?

A Virtual Machine is exactly what it sounds like, a virtual computer. Using a virtual machine you are able to run multiple operating systems at once. It achieves this by emulating real computer hardware virtually. This lets us install Linux without touching our main system until we are ready.

We will be using VirtualBox for this tutorial as it is FOSS and easy to use, but other options exist.

## Setting up VirtualBox

You will want to download VirtualBox from their [website](https://www.virtualbox.org/wiki/Downloads) or you can use a package manager like [chocolatey](https://www.blog.mattlamont.com/chocolatey-package-manager-for-windows/). During the installation it might reset your network adapter as it installs its own drivers, don't worry if you lose internet for a few seconds during the install.

Once you open it you will see something similar to this:

{{< figure src="./img/testLinuxVirtualMachine_VBox_StartPage.png" alt="Virtualbox Start Page">}}

You will see that I already have two Linux virtual machines, but we can add one more. 

To create a Virtual Machine we first need to download a disk image of the Linux distribution we want to test. So for this example, we will [download Linux Mint](https://linuxmint.com), a great beginner-friendly Linux.

After downloading the Linux Mint ICO file we can start making our new VM.

### Creating a new Virtual Machine

{{< figure src="./img/testLinuxVirtualMM_CreateVM_1.png" alt="Virtualbox Create Page">}}

To get started we will press the **blue gear/star button**. This will bring up a window that will let us create a new VM. To start we need to give it a name. I will call this one Linux Mint. Next, we will put it in a folder, I like to keep all my virtual machines in one location for easier organization. Finally, we will set the type to Linux and the version to Ubuntu (64-bit). We are setting it to Ubuntu because Linux Mint is based on it and Virtual Box doesn't have a dedicated Linux Mint option.

Next, we will set the memory size. This will depend on how much RAM you have and how much you want to give to the VM. I usually set this to 4 GB for 64-bit Linux distros. Setting this to less than that might make the VM run slowly depending on the distro.

On the Hard disk page, we will want to click on "Create a virtual hard disk now" this is the file that you will store your VM and all its files. You can select VDI for the file type. Dynamic size is what I usually use as it saves space, but you could use Fixed size to increase the speed of the virtual machine.

Most Linux distros only need around 15 GB of storage space to install and function. I am going to use 20 GB for this distro in case I want to install extra software afterward.

Now you can see we have a virtual machine named Linux Mint.

{{< figure src="./img/testLinuxVirtualMachine_VBox_StartPageWithVM.png" alt="Virtualbox Start Page">}}

### Starting Up the VM

Before we start up Linux Mint we need to let VirtualBox know where the disk image is. In the storage section of the main window, you will see "IDE Secondary Device 0". Click the text "Empty" and then "Choose a disk file..." this will bring up a file selection box. Find the Linux Mint ICO we downloaded earlier.

Now we just need to press the Start button.

## Running Linux

{{< figure src="./img/testLinuxVirtualMachine_VBox_GRUB.png" alt="Virtualbox Start Page">}}

Once you hit start you will see a screen like this pop-up. This screen gives us a lot of options before installing Linux mint, but we will just Start Linux Mint through the first option in this tutorial. Now you just need to wait for a bit while Mint boots.

You will notice two notifications at the top of the screen one saying that the keyboard auto-capture is on and another saying that the virtual machine supports mouse pointer integration. The first is just saying that the VM will use your keyboard whenever it is active. The second just means that the mouse pointer does not get locked to the VM while you are using it. You can close it.

### Live CD and Installation

Notice the Install Linux Mint icon on the desktop? Yep, that is the way you will install the OS inside the virtual machine. That said most Linux distros can run without installing them in a mode we call a Live CD. You don't need to install it to test it out, but you will get better performance and be able to save data by installing it.

### Installing Linux

Let's try installing Mint inside our virtual machine. The first thing you will do is set the language and keyboard layout. 

Next, you will be asked if you want to install the multimedia codecs. These are needed if you want to watch video on some websites and some video file types.

{{< figure src="./img/testLinuxVirtualMachine_VBox_Partitioning.png" alt="Virtualbox Start Page">}}

Now we are at the part that confuses many people: The Installation Type page.

Inside this virtual machine, we don't really need to worry about it, but if you are installing it on real hardware you might want to back up your files and try dual booting if you already have another OS installed on the system.

In this tutorial, we will just "Erase disk and install Linux Mint". Then we can click on the **Install Now button**.

There will be a popup that gives you a list of changes that will be made and ask if it is okay to make these changes. We are going to press **Continue**.

### Time Zone

{{< figure src="./img/testLinuxVirtualMachine_VBox_TimeZone.png" alt="Virtualbox Start Page">}}

The next page lets you choose your timezone. You can either click on the map or type your location into the text box. You can change this later if you wish in the Linux Mint settings.

### First Linux User

After setting your timezone you will be able to create your first user. This is how you will sign into your computer.

{{< figure src="./img/testLinuxVirtualMachine_VBox_CreateUser.png" alt="Virtualbox Start Page">}}

*   **Your name**, this might be used by some applications to display your name such as email clients.
*   **Your computer's name** is the name of the computer on the network. It might not be very important in this virtual machine, but having good names for your devices can be useful when trying to manage your network.
*   **Username**, your username will be the one you enter to login to your computer, just like on Mac or Windows.
*   **Password**, use a secure password for your account. The first user on a system usually has administrator access that can be used with this password, make sure it is strong. We will go over how Linux administrator accounts work in a future article.
*   **Log in automatically** will do what it says. Rather than requiring a password you will automatically be logged in when you start Linux Mint. This might be useful if the computer does not store personal information. If this is a personal computer I would recommend keeping the option on **Require my password to log in**.
*   **Encrypt my home folder** will encrypt your home folder. The home folder is where all your user files are stored, it is like **users** in windows. Normally Linux does not encrypt this folder. If you want extra security you can encrypt the folder so files can only be accessed when logged in. This is probably not necessary for the majority of people, but use it if your threat model requires it.

Now you just need to wait for the installer to finish installing Linux.

### Congratulations You have Installed Linux in a Virtual Machine

All you have to do now is remove the disk from the virtual machine and restart it. 

Now you can start tinkering with Linux Mint before installing it on your hardware. The performance will not be as good as if you installed it on the computer itself, but it will give you a chance to taste the Linux world without having to commit.

In the future, we will explore how Linux works and take one step closer to gaining our digital independence from big tech.
