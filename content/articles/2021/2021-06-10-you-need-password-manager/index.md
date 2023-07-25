---
author: Matthew
categories:
- Introduction to Computers
- Tech Tips
date: "2021-06-10T13:57:33Z"
featuredImage: ./img/you_need_passwrd_manager_feature.png
tags:
- Cross-Platform
- FOSS
- Free Software
- Open Source
- security
title: Why You Need a Password Manager
aliases:
  - /you-need-password-manager/
slug: /you-need-password-manager/
---

We use passwords everywhere to secure our important accounts, but how secure are your passwords? A password manager does what the name implies: it manages your passwords. Today, we are going to look at how they work and how they improve our security.

## The Problem with Passwords

Passwords are designed to keep our accounts safe as long as we follow some basic best practices.

Passwords should be:

*   At least 12 characters
*   Contain a mix of uppercase, lowercase, numbers, and symbols
*   Unique to each account or device
*   Not contain words from a dictionary
*   Not contain personal information such as birthdays, names of family, etc.
*   Should change regularly depending on the sensitivity of the account

These are easier said than done. How many accounts do you have between your personal life and work? 5, 10, 100? Imagine remembering 100 different passwords that had to follow all of these requirements. That's not possible for most people. This leads to people using the same password across all their accounts. When one of them gets compromised all their accounts do, but they never notice.

Password managers help fix this problem.

## What do Password Managers do?

{{< figure src="./img/keyStock.jpeg" alt="Image: The master password is the key to your passwords.">}}

Password managers are applications that store and organize passwords. Your passwords get stored in an encrypted database that holds a list of your accounts, passwords, and other supplemental information. This database is secured using a master password. This password is like a key to your password vault. You only need to remember one password instead of 100.

Most password managers include tools for generating secure passwords, have apps for all major platforms, and include browser plugins. Many also can autofill forms on websites and log in for you.

## Types of Password Managers

There are two major types of password managers: Ones that store your passwords locally, and ones that store them in the cloud. What you use will depend on your threat model and how much convenience you are willing to sacrifice for security.

### Cloud Password Managers

Cloud password managers store your passwords on a server somewhere on the internet. This might be controlled by a company or hosted by you. This makes it easy to sync your password across many devices and many providers offer extra services on top of providing password storage. This is incredibly convenient, but it does come at the cost of security.

You have to trust someone when you use a cloud password manager, this is often the company that makes the password manager or a webhost if you are running your own. This is usually okay, as your passwords are encrypted on your machine, but it's something to keep in mind.

#### Best Cloud Password Manager: [Bitwarden](https://bitwarden.com/)

{{< figure src="./img/bitwardenWebsiteMainPage-1.png" alt="Image: Bitwarden is a cloud password manager.">}}

I'd recommend the cloud password manager , if your threat model allows for it. I use Bitwarden on a daily bases for most of my accounts. It supports all major platforms and web browsers, it is [FOSS](https://www.blog.mattlamont.com/what-is-free-and-open-source-software-foss/), and you can host your own copy of it on your own servers if you don't trust Bitwarden's servers.

Bitwarden has a mobile and desktop app, as well as a browser extension for all major browsers. This means your passwords will be available to you anywhere. It can store personal information such as address and card numbers, making it easy to auto-fill online forms.

Bitwarden is free, but it does offer a premium service that includes encrypted file sharing and hardware token support. Most people don't need these features, but it is a great way to support the open source project.

Warning: Don't use LastPass. LastPass is one of the most popular proprietary password managers out there and you will often see it in online recommendations. It's free tier is almost useless as it limits what kinds of devices you can use it on and it is a closed source system. Never trust closed source tech with more data than necessary, use Bitwarden instead.

### Local Password Managers

Local password managers save your passwords in a database stored on your device. This is significantly more secure in theory than using a cloud based password manager, but it can be really inconvenient, as you will have to come up with your own way to sync passwords across devices, such as a NextCloud server. Use a local password manager if security is your highest priority.

#### Best Local Password Manager: [KeePassXC](https://keepassxc.org/)

{{< figure src="./img/KeePassXC_MainPage.png" alt="Image: KeyPassXC is a local password manager.">}}

KeePassXC is a cross platform and FOSS password manager that works on your desktop. It has many powerful features including hardware token support, browser integration with all major browsers, and can keep track of personal data alongside passwords. KeePassXC does not have an official mobile app, but their are third party apps for that.

KeePassXC is based on another FOSS desktop password manager called [KeePass](https://keepass.info). KeePass is a great password manager, but it is not officially cross-platform and was designed for windows.

I do not use KeePassXC or any other local password manager on a daily bases, so take this recommendation with a grain of salt.

There are KeePass compatible android apps on F-Droid, and the KeePass download page keeps track of some ports. Just remember that they are developed by independent developers unaffiliated with KeePass and KeePassXC.

[F-Droid List](https://search.f-droid.org/?q=keepass&amp;lang=en)

[KeePass Compatible Software List](https://keepass.info/download.html)

There are other password managers out there and we will write an article about them in the future, but these two are the best that we have used.

## Limitations of Password Managers

Password managers are great, but they do have some weaknesses to keep in mind:

You are replacing tens if not hundreds of passwords with a single master password. This is a single point of failure, so it is critical that you use a secure master password. It is important to use two-factor authentication whenever possible and never share your master password with anyone.

Cloud based password managers put your database in the hands of another entity. This is usually a non-issue, as any password manager worth its salt will do encryption on the users end and have no access to the actual unencrypted passwords. Just make sure that the server code has been audited.

I've said multiple times in the past to not use closed source tools for sensitive data, and I stand by it. Password managers hold the key to your digital life. Proprietary apps have too many issues: You cannot audit them, the terms of service can change on a moment's notice (like it did with LastPass), and you could lose all your passwords if the company managing them shuts down. It's not worth the risk.

## Password Managers are the Best Way to Handle Passwords

We use passwords everywhere to protect our digital lives, so it's imperative that we protect them. The problem is, we're bad at keeping track of them and using the best practices to keep our accounts secure. Password managers can help by keeping tack of the many accounts we create. Check out Bitwarden and KeePassXC, and see what works for you.

Please share your experiences with password managers with us in the comments below. 
