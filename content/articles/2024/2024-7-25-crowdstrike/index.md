---
title: "CrowdStrike"
date: 2024-07-25T08:20:59Z
authors: 
- "Matthew Lamont"
draft: false
tags:
  - Windows
  - Security
slug: /crowdstrike/
keywords:
  - CrowdStrike
description: CrowdStrike's negligence lead to the largest outage to date, but it isn't the first time and it won't be the last. 
---

CrowdStrike released another bad update to their Falcon sensor, this time taking out enough systems to make it into headlines.

Before we get into what happened a little background. 

## What is CrowdStrike and their Falcon Sensor?

CrowdStrike provides cybersecurity products for enterprise customers. Think anti-virus, data recovery, training, etc, but very expensive and they do a lot of the work for you when you need to prove to a government agency that your system is compliant with security requirements.

Their Falcon Sensor is a kernel level endpoint security software. Think anti-virus on steroids. As this software runs at the kernel level it can see everything running on your computer, detect what actions software is doing, and in theory directly access the hardware. This can be very useful, but also gives Falcon unfettered access to your computer systems. You have to really trust that CrowdStrike knows what they are doing and test their software before sending out updates.

## What Happened?

It looks like CrowdStrike does not test their software. A faulty update was sent out last week that caused Windows' kernel to crash (blue screen of death). As Falcon runs when the system boots up it will crash the system whenever Windows loads making it hard to recover from. 

To fix the issue you would have to boot your system in safe mode and manually delete a Falcon driver file from your Windows directory. This usually means someone from a organizations's IT will need to physically access the device to fix it. This is why it is taking so long to fix for some organizations to recover. 

On many system Falcon was setup to auto update. This lead to a good chunk of the world's Windows computers going down on Friday.

This took down airlines, government websites, major companies entire networks, hospitals, and even emergency response call centers. 

There were people who couldn't get help they needed because CrowdStrike didn't test their update before releasing it. They released it right before the weekend knowing that IT staff might be out or have to work overtime to manually fix the issue. Some systems are still offline as organizations try to fix the issue.

## It has Happened Before and can happen on Linux

What is even more insulting about this is that Falcon had two other major incidents earlier this year where they sent out bad updates.

A [post](https://news.ycombinator.com/item?id=41005936) on Hacker News claimed that their Linux fleet was taken down on April 19th by a bad Falcon update.

In May users of [Rocky](https://forums.rockylinux.org/t/crowdstrike-freezing-rockylinux-after-9-4-upgrade/14041)/[Redhat](https://access.redhat.com/solutions/7068083) Linux also reported kernel panic with a bad update.

While CrowdStrike claims that they test their software, I have doubts.

## My Take

I am blessed that my company doesn't use CrowdStrike, but many of our clients are still recovering. I work in IT in the medical field so it is not a trivial issue. Lives might be at stake due to this update.

Enterprise businesses have to worry about compliance, ease of implementation, and security of a product. They can't just use some random open source code nor can many of them afford to write their own security software and get it certified. Because of this many are stuck using proprietary software that they don't understand and can't control. Not using any security software is out of the question, but maybe they should start looking for alternatives.

While I do think Falcon is proprietary garbage, it is necessary for many organizations. The thing is, there are alternative tools out there for endpoint security. The reason so many devices were taken down was because there was a single point of failure, they were all using Falcon. We need competition to help prevent this from happening again in the future.

Organizations also need better education on what the software they run is doing. It is one thing to pay for security software because it checks a compliance box and another to actually understand what it is doing. If organizations understood they were installing a kernel level tool and what that can mean if it breaks they may have had better contingencies. They might of also not had it auto update on their servers.

There is no reason to release the updates on a Friday night unless they are mission critical or you are hoping no one notices issues with it till Monday. CrowdStrike should not be releasing updates at the end of the week and organizations shouldn't be automatically applying them either. Proprietary software has proven to be unreliable, expensive, and untrustworthy. We should treat them as such and test everything before deploying it out to all other systems.

Ultimately this was CrowdStrike's fault and not the organizations that use it. Enshitification seems to be a trend for all things, even software that hospitals rely on.  

CrowdStrike will hopefully see some legal repercussions. I don't see a way that this was not caused by negligence on their part. In a just world their leadership would face criminal charges for what has happened, but we live in a capitalist dystopia. Instead they are sending out [$10 Uber Eats gift cards](https://techcrunch.com/2024/07/24/crowdstrike-offers-a-10-apology-gift-card-to-say-sorry-for-outage/) to some of their partners as an apology. They should be using that money to hire a QA team, do some testing, and compensate everyone who was impacted by this, not insulting us with this fake apology.

My heart goes out to all of you who have been effected by the outage. There is no world where something like this should have happened nor will any remedy that CrowdStrike provides ever be enough undo the damage they've done.
