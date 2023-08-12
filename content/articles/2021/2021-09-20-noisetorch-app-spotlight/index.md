---
authors: 
- "Matthew Lamont"
categories:
- App Spotlight
- Linux
- Tech Tips
date: "2021-09-20T07:41:00Z"
featuredImage: ./img/noiseTorch_Select_CoverImage.jpeg
tags:
- Audio
- Free Software
- Linux
- Open Source
title: NoiseTorch | App Spotlight
aliases:
  - /noisetorch-app-spotlight/
slug: /noisetorch-app-spotlight/
---

[NoiseTorch](https://github.com/noisetorch/NoiseTorch) is a small [FOSS](https://www.blog.mattlamont.com/what-is-free-and-open-source-software-foss) Linux app that removes background noise picked up by your microphone. It creates a virtual microphone that isolates vocals. This is great if you are in a noisy environment when on a call or recording a video. Let's take a look at how it works.

## Setting Up NoiseTorch

NoiseTorch is easy to install. If you are on Arch or a derivative, you can find it in the AUR. 

On other distros, you can install it by following the instructions in the [GitHub readme](https://github.com/noisetorch/NoiseTorch/blob/master/README.md): 

1.  Download the [latest release](https://github.com/NoiseTorch/NoiseTorch/releases) from GitHub.
2.  Unpack the file:  
```tar -C $HOME -xzf NoiseTorch_x64.tgz```
3.  Give it permissions needed to run:  
```sudo setcap 'CAP_SYS_RESOURCE=+ep' ~/.local/bin/noisetorch```

There may be some extra steps depending on your setup, so consult the readme for more info.

I'm running Manjaro, so I downloaded the binary from the AUR.

## Using NoiseTorch

Now that we have NoiseTorch installed, we can start using it. Launch it and we will be greeted with a screen that looks like this:

{{< figure src="./img/noiseTorch_Select_Microphone.jpeg" alt="Image: NoiseTorch input device selection screen.">}}

All you have to do is select Filter Microphone and select the microphone you want to filter background noise out for. After that, you just need to select "Load NoiseTorch" and change your audio input device to your new NoiseTorch Microphone. Now it will start isolating noise.

Here is a sample of my audio to compare the two:

NoiseTorch Sound Isolation On:

{{<audio src="/audio/NoiseTorchAudioTest_Isolated.ogg">}}

Blue Yeti Microphone Without Sound Isolation:

{{<audio src="/audio/NoiseTorchAudioTest_Not_Isolated.ogg">}}

Can you hear the difference? Both clips were recorded in my living room next to my home server. It's amazing what a difference such a small application can make.

## Limitations

There is no silver bullet for all audio issues. NoiseTorch doesn't work perfectly. I've noticed that it will sometimes cut off "s" sounds if they last too long, and there is slight latency with the audio recording. Neither of these should be an issue for most people, but it's something to keep in mind. 

This app is great for helping to keep background noise down after you've already done everything you can to remove background noise. 

Give it a try and consider donating to the developer of this amazing app.
