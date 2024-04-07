---
title: "March Website Updates"
date: 2024-04-07T11:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
tags: 
- Website Updates
slug: march-website-update
keywords: "Website Update"
description: New Light Theme, better home page, and a lot of under the hood speed improvements.
---

As a natural tinkerer I can't just leave the website code alone so if you come here often you have likely noticed some changes to the website.

Here are some of the thinks I've been working on.

## Improved Performance

Accessibility is very important and one thing that limits access to the internet is web pages that are multiple megabytes in size for no reason. Not everyone has high speed internet and some people even pay for metered data connections. If it takes 20 MB to display some text on the screen that means users can be waiting a while for your website to load and they might be paying for each one of those MB too.

To that end I've reduced the size of every page on this site to below 1MB and in some cases below 512KB. How?

### Image Optimization

#### Converting to JPEG and webp

A lot of images on this site were in unoptimized PNG and JPEG format. To fix this issue I did a few things.

First I converted every image on this site into webp and an optimized JPEG. This can be done with imagemagic using the following commands in the same directory as your images:

``` sh
magick mogrify -format jpeg -sampling-factor 4:2:0 -strip -quality 80 -interlace JPEG -colorspace sRGB *.png *jpg 
magick mogrify -format webp -quality 82 *.png *jpg

```

Replace the *.png and *jpg with the file extensions you want to search for and replace.

The first commands finds all png and jpg images and reformats them into interlaced jpg files at 80% quality. It removes any profiles and comments, resamples the images, and sets the colorspace to sRBG.

The second command is a little simpler and just converts the png and jpg images into webp at 82% quality.

I did this for every image on the website so all images are now in both JPEG and webp format. 

JPEG is a long supported format and the images are usually smaller than a PNG at the same quality. This means that users with out of date web browsers should be able to see the images without issue.

Webp is a more modern image format that is even smaller than JPEG. If your browser supports modern image formats then you will get these images instead of the JPEG versions. 

This means webpages that load faster and take less bandwidth for both my hosting provider and my readers.

#### Making Hugo Display the Right Images

Originally my images were declared with their file extension. This meant that I could only ever use one version of an image. If I used webp it would mean breaking my website for users with older browsers and if I used just JPEG it would be leaving performance on the table.

Fortunately HTML has a ```<picture>``` element that lets you have multiple formats. If the browser supports webp it will download and display the webp version and if not it will load the JPEG. Naturally if your browser doesn't support images you will see the alt-text.

To add this I overwrote Hugo's default figure shortcode's img element:

``` go
<picture>
    <source srcset="{{ $src }}.webp" type="image/webp" />
    <img src="{{ $src }}.jpeg"
    {{- if or (.Get "alt") (.Get "caption") }}
    alt="{{ with .Get "alt" }}{{ . }}{{ else }}{{ .Get "caption" | markdownify| plainify }}{{ end }}"
    {{- end -}}
    {{- with .Get "width" }} width="{{ . }}"{{ end -}}
    {{- with .Get "height" }} height="{{ . }}"{{ end -}}
    {{- with .Get "loading" }} loading="{{ . }}"{{ end -}}>
</picture>
```

In all my figure shortcodes across this website I removed the file extension as I hardcoded the extensions in the shortcode. This has the negative side effect of breaking images if I don't have both the jpeg and the webp in the source directory. I am sure I could add more conditions and do something to clean it up in the future, but this works for now and I have not seen other guides on how to do this in Hugo.

### Removing Unneeded Scripts

The default theme for this website incudes a lot of JavaScript for features I don't use. For that reason I removed them as well as the broken search feature.

I have nothing against useful JavaScript, but it is rude to waste people's bandwidth with scripts that don't do anything or are unneeded.

## New Light Theme

Another thing I've been working on is a new theme. It is still rough around the edges (links lack contrast, colors don't display right on all screens, etc.), but we are getting somewhere with it.

The Poison theme that this site is based off of has a very white default light theme. Most of the people I know used the dark theme because the light mode was too bright.

I've started to put together a new light color scheme. The goal is to be warm, cozy, and reminiscent of green tea.

In the future the dark theme is going to get a revamp as well and will be themed after red/black tea. 

Share your thoughts and let me know if you have any color ideas that could improve either. I'm not a color guy so this is still very much a work in progress.

## New Homepage

I was told by multiple people that there was too much text on the home page that. All the links were pushing the page up to where it might have gone over 1MB as well. 

With that in mind I rewrote how I'm getting the list of pages. Each content type is now displayed separate from one another and only shows the last 5 articles from each category. It is fully responsive and should make it easy to add or remove content types in the future.

Let me know if you think there is anything I can do to improve it further.

## Star Rankings in Reviews

I wrote a small note on how I [added Star Rankings to my reviews](https://techtea.io/notes/2024/03/adding-star-reviews/). This is just a start as I noticed they don't appear in text based browsers as I use CSS to create the stars. In the future I think I'll try using Hugo's go templates to generate the stars as plain text, then apply the gradient to them using CSS for the fractional fill. This way people browsing in lynx can still see the stars, just not as accurately.

## More to Come

I love to tinker with the website so more things will change in the future. Finishing the Light and Dark color schemes are fairly high priority as I want my website to be a more cozy place on the internet. 

I am also working on more articles regarding personal websites. Hopefully they will be a resource others can use to make far more amazing websites than I could ever imagine.

There is also plans to add a blogroll and a link/bookmark blog to the website so I can help make it easier to find cool things on the web.
