---
authors: 
- "Matthew Lamont"
categories:
- Tech Tips
- Windows
date: "2020-09-20T12:30:00Z"
featuredImage: ./img/choco_CLIFeaturedImage-1
tags:
- Command Line
- FOSS
- Open Source
- Productivity
- Windows
- Tutorials
- App Spotlight
title: Chocolatey Package Manager for Windows
aliases:
  - /chocolatey-package-manager-for-windows/
slug: /chocolatey-package-manager-for-windows/
---

[Chocolatey](https://chocolatey.org/) helps solve one of the biggest issues working on a Windows machine: Software Management.

It's easy to maintain and update software on most other operating systems. On Mac you have Homebrew, on your phone you have app stores, and on Linux and BSD, you have package managers. You can install software in one easy step. Windows, on the other hand, has you go to the website for the software, download it, run an installer, and then remember to install updates later.

Chocolatey is a package manager for Windows that helps alleviate these issues.

## What is Package Management?

Chocolatey, dpkg, and Homebrew are all software management tools we call Package Managers. A package is an archive file that contains a program and the data for that program to run. These packages are then put in a server (repository) where users can download and install them, like the App store.

Your package manager can detect all the software you installed with it, what version you have installed, and if a new version of the software has been pushed to the repository. Essentially, it can automate software installation, removal, and updates for you.

A package manager saves you time managing software so you can focus on using that software instead.

Warning: Chocolotey uses a public repository. While packages are generally safe and moderated, you are putting your trust in a third party to deliver you the software you need. Only download software you trust.

## Installing Chocolatey

1.  Open PowerShell in Administrator mode. You can do this by right clicking on the Windows logo on the taskbar and clicking "Windows PowerShell (Admin).
2.  Copy the following command and run it in powershell:  
```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))```  
This will set the ExecutionPolicy to Bypass, then download and install Chocolatey. You can read more about Execution Policies on [Microsoft's documentation website](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7).
3.  If you see no errors, you can test Chocolatey by typing ```choco``` into Powershell. It should print the version number.

Installing Chocolatey is that simple. If you need more information, you can find it on the [documentation website](https://chocolatey.org/install).

## Using Chocolatey

Chocolatey can be used from either PowerShell or via the Chocolatey GUI. We'll be using PowerShell for this tutorial, and will cover the GUI in a future article.

Powershell gives you full access to all the features Chocolatey has to offer in an easy to use command line tool. We will go through some of the basic commands here, but you can look at the built in help file or [online documentation](https://chocolatey.org/docs/commands-reference) for more info.

### Instating Applications 

To install an application, we'll need to run a simple command in an Administrator Level Powershell window.

```choco install <PkgName>```

To install Firefox, we would run the command ```choco install firefox```.

{{< figure src="./img/choco_CLIInstallSoftware" alt="Image: Installing Firefox with Chocolatey">}}

Each time you install an application, Chocolatey will prompt you for permission to run a script. You can press "Y" and then "ENTER" to run the script, or "A" to run all scripts that will be run as a result of the command. Using the All function can be very useful when installing multiple packages at once.

### Uninstalling Applications 

Uninstalling applications is just like installing them in Chocolatey:

```choco uninstall <PkgName>```

So to uninstall Firefox we could simply type ```choco uninstall firefox```. 

{{< figure src="./img/choco_CLIUninstallSoftware" alt="Image: Uninstalling Firefox with Chocolatey">}}

This will remove the program from your system, but make sure you read the script description carefully, as there might be other steps for removing the software you have installed.

### Updating Applications 

Updating applications in Chocolatey is just like the other commands, but with a small twist. We can upgrade all of our programs by specifying "all" as the package name. This will update all programs installed on our system with Chocolatey. 

```choco upgrade all```

This can take a while, so you might want to upgrade the packages you need right way first before using an "all" command. Chocolatey will only update the applications that aren't already up-to-date, so you don't have to worry about redownloading everything.

{{< figure src="./img/choco_CLIUpgradeSoftware" alt="Image: Updating all packages with Chocolatey">}}

### Finding Software 

The easiest way to find what packages are available in Chocolatey is to search using your favorite web browser. This helps you get more detail on what packages are available and helps you sort through packages that have the same name. There is also a way to search the repository within Chocolatey.

You can use the list/search command to find a list of packages that match a search query:

```choco search <query>```

If you only type "choco search" it will look at all software in the repo.

"choco search node" will look something like this:

{{< figure src="./img/choco_CLIFindingSoftware" alt="Image: Searching Chocolatey repo for software">}}

There are many other commands, but they will be covered in a future article.

## Take Control of Your Software

Chocolatey gives you back control of the software installed on your computer. You can install, update, and manage all your applications in one place with just a few simple steps.

In the future, we will go over the Chocolatey GUI and advanced features.
