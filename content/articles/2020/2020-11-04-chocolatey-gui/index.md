---
authors: 
- "Matthew Lamont"
categories:
- Tech Tips
- Windows
date: "2020-11-04T11:30:00Z"
featuredImage: ./img/choco_GUIFeaturedImage
tags:
- Command Line
- FOSS
- Open Source
- Productivity
- Windows
- Tutorials
- App Spotlight
title: Chocolatey GUI | Chocolatey for the Average User
aliases:
  - /chocolatey-gui/
slug: /chocolatey-gui/
---

[Chocolatey](https://chocolatey.org) is a great application for managing your installed programs on Windows, but it's not always the easiest to use. Chocolatey GUI gives you an easy graphical interface to update your programs without having to use the command line. Today, we are going to install the GUI and perform all the regular tasks we showed you in the previous article.

## Getting Started

Make sure you have Chocolatey installed before we get started; see our [previous article](https://www.blog.mattlamont.com/chocolatey-package-manager-for-windows/) if you haven't already. We are going to install the GUI using PowerShell and the following command:


```choco install chocolateygui```

You can find Chocolatey GUI in the start menu once the installation is finished.

## Navigating Chocolatey GUI

{{< figure src="./img/choco_GUIOverview" alt="Image: Chocolatey GUI Overview.">}}

The GUI is split into 3 major section:

*   On the left, you can see your sources. This is where you can find what applications are installed on your system and check the programs available in the Chocolatey repo.
*   On the top, you have a tool bar where you can search for packages and update all of your existing ones.
*   Below the toolbar, you have a list of packages. This section lets you update, install, remove, and see the details of packages.

### Finding and Installing Packages

{{< figure src="./img/choco_GUIfindingAndIndstallingPackages" alt="Image: Finding and installing Packages in Chocolatey GUI.">}}

Installing packages takes just a few easy steps in the Chocolatey GUI. 

1.  Click on the source you wish to download packages from in the sidebar. In most cases this would be "chocolatey".
2.  Search for the package you want to install using the tool bar. You can double click to bring up more details if you wish.
3.  Right click the package and click install or click the "Install" button on the details page.

### Removing Packages

{{< figure src="./img/choco_GUIRemovingPackages" alt="Image: Removing Packages in Chocolatey GUI.">}}

To remove a package you installed in with Chocolatey, you can right click on the package and click "Uninstall". This can be done from either "This PC" or in the repo tabs on the sidebar. You can also do this from the details view.

### Updating Packages

{{< figure src="./img/choco_GUIupdatePackages" alt="Image: Updating Packages in Chocolatey GUI.">}}

Chocolatey GUI allows you to both update packages individually or all at once. You can update all your packages with the button on the tool bar next to the refresh button. It looks just like the refresh button, but has an asterisk next to it. You can update a package individually the same way you can uninstall or install one, either by right clicking or on the details page.



### The Details Page

{{< figure src="./img/choco_GUIpackageDetails" alt="Image: Package Details in Chocolatey GUI.">}}

There is a lot that you can do with Chocolatey, and the GUI makes it easier in some ways.

The details page is particularly interesting. It displays almost all the information you need to know about a package including:

*   Author
*   Project Website and License links
*   The package maintainer
*   The description from the page on the Chocolatey website.
*   Release notes.
*   A tool bar on the bottom that lets you Install, Reinstall, Remove, and Update packages

## Chocolatey GUI is easy

Chocolatey's command line interface is extremely powerful, but it can be intimidating if you are not use to the command line. The GUI gives most of that power a much friendlier interface for customers, kids, and the less tech savvy.

In the future we will cover some of the more advanced activities you can accomplish with Chocolatey.
