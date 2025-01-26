---
title: "Manage Secrets in KDE Wallet"
date: 2025-01-26T12:50:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Tech Tips
  - KDE
  - Linux
  - App Spotlight
slug: /manage-secrets-kde-wallet
keywords:
  - KDE Wallet
  - Manage Secrets
description: Today we will look at how to use KDE Wallet to store secrets on Linux.
---

So I'm going through my config files (dot files) for programs I use this morning and some of my secrets (passwords, API keys, etc) are saved as plain text in the config files. Not the best practice, even if they are passwords for non-critical services.

I want to backup my dot files and make them accessible to anyone who wants them, but that is not happening till I fix the issue. To remedy this I was looking at ways to store my secrets at rest and found that I can use [KDE Wallet](https://apps.kde.org/kwalletmanager5/) for this fairly easily. I use KDE as my desktop environment of choice so I already had it installed.

## What is KDE Wallet

If you use the KDE desktop environment you probably have been prompted once or twice to enter your password into KDE Wallet. This is KDE's built in password manager. By default it stores your passwords for WiFi networks, KDE applications, and your Online Account integrations, but you can use it with pretty much anything. 

In the past KDE wallet would ask you to unlock it with a password every time you logged into the computer, but nowadays most systems are configured to automatically unlock when you login to the system. Unfortunately the bad reputation has stayed with it despite how useful it has become, don't listen to the complaints till you've tried it. 

If you use KDE you probably have this installed already, but if you don't you may need to look for KDE Wallet Manager in your distribution's repository.

## Using KDE Wallet

If you don't care about using it for more than the default stuff then you don't have to do anything. If you want to use it for storing your browser passwords (chromium only right now and I'd still use Bitwarden instead) and storing secrets for your scripts (something I'm doing now) you can with very little extra work. 

Today I'm only going to go over the basics of using KDE Wallet to store and retrieve passwords from the terminal as that is what I'm using it for.

### KDE Wallet Manager

Once you have KDE Wallet installed you will be able to open the KWallet Manager program and you will be greeted with a window similar to this depending on your KDE theme.

{{< figure src="./img/kwalletmanager" alt="Image: KDE Wallet Manager for managing your secrets.">}}

The **Contents** tab is where all your application secret are stored, ie. passwords, API keys, ssh keys, and anything else that you want saved.

The **Applications** tab shows the programs that are currently using the wallet. 

You can have multiple wallets. If you run KDE there is a settings page under your system settings to create new wallets and manage them, but for today we are going to be using the default *kdewallet* as the defaults are good for what we are doing today.

I'm going to create a new password to store my *Miniflux* authentication token so I cna access it later in my newsboat configuration file.

To do so you are going to expand the Passwords folder in the left sidebar to reveal a Passwords subfolder (bad naming convention, I know), the right click on the Passwords folder and click new. You can name this new entry whatever you want as long as you remember it. Then click **Show Contents** on the right hand box to reveal a text entry field. Type whatever you want to store in there and hit save.

Once you saved it you can now access that password any time by opening your KDE Wallet and taking a look, but that wouldn't be very useful so we are going to move onto the real star of the show, the terminal command.

### Accessing your Wallet via the Terminal

The whole reason I did this was to help remove secrets from config files like my newsboat config. To do that I need a way to access the KDE Wallet password from anywhere on my system and that is where the `kwallet-query` command comes in. This will let you query any of your kde wallets for values. To access my miniflux password for example all I need to do is type:

``` sh
kwallet-query -r miniflux kdewallet
```

The `-r` flag tells the program to read an entry from the wallet, `miniflux` is the name of the entry, and `kdewallet` is the name of the wallet we want to access. You might be prompted to enter your wallet password if it isn't open, but as long as you are using your default wallet it should be open when you first login to your computer.

### Creating Entries from the Terminal

You can use `kwallet-query` to write to a wallet as well using the `-w` flag. For example I want to store "text" as a value into a password named bob. I can do that using the following commands:

``` sh
echo "text" | kwallet-query -w bob kdewallet
```

The `-w` flag takes standard output for its value so I `echo` out the word "text" and pipe the output into `kwallet-query`. `bob` is the name of the password and `kdewallet` is again the name of the wallet. By default `kwallet-query` saves the password to the **Passwords** folder, but you can specify any password using the `-f` flag. 

Because the tool uses standard out you can generally save anything to a KDE wallet, making this useful if you are scripting in a kde environment. It supports key value pair maps as well if you pass it JSON. If you are unfamiliar with pipes I highly recommend you read up on the basics as this is what makes terminal applications so powerful.

### Using it in Newsboat

I use Newsboat for my desktop RSS reading and use Miniflux as a backend server for managing all my RSS feeds. Before using KDE Wallet I was saving my Miniflux token as plain text in my Newsboat config file. Fortunately Newsboat lets you use the output of commands as the password in your config file. I switched my not so super secret token for the following in the config file:

``` sh
miniflux-tokeneval "kwallet-query -r miniflux kdewallet"
```

Not the most elegant and will only work on systems with KDE wallet, but it works and that is what matters right now.

## This isn't a Perfect Solution

Different systems use different password keyrings/secret managers and KDE Wallet isn't a password manager I'd use for general passwords. This solution is KDE specific and probably won't work if you don't want KDE packages on your system. This will not work on Mac or Windows either. 

If you use Gnome for example you will be using the Gnome Keyring by default instead of KDE Wallet. In that case the best solution is to switch to KDE obviously, but if you can't do that there is documentation on how to do the same thing with Gnome.

You can do the same thing I did with a more universal password manager like BitWarden, Pass, or KeyPass to manage both your normal passwords and secrets to avoid headaches. 

If you use KDE though you will probably find this an easy solution to the problem of storing secrets in config files. Then again I'm sure there are some programs that don't have proper integration with standard password toolchains. 

## Further Reading

This system is fairly straightforward, but The Arch Wiki has a lot of [great information on the tool](https://wiki.archlinux.org/title/KDE_Wallet) that can help even if you aren't running Arch.

You should also consult the man pages for `kwallet-query`. Never underestimate the man pages, they are your friend and don't require internet to know what you are doing. 

I'm going to be learning some Bash this year and using more terminal based apps in general so expect more of these kinds of articles in the future.
