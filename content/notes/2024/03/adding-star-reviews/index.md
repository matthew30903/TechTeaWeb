---
title: "Adding Star Rankings to my Reviews"
date: 2024-03-28T11:02:53-07:00
draft: false
authors: 
- "Matthew Lamont"
tags: 
- Website Updates
slug: adding-star-reviews
keywords:
- Star Reviews
description: Making my reviews easy to parse is important. I recently added star rankings in my Hugo blog. Here is how.
---

I always hated five star review systems, they are almost always useless and lack nuance to really tell people anything about the product. 

That said, my review template was kinda bland and not easy to parse. Star rankings would make it easy to know how I feel about a product at a glance and everyone already knows my reviews are highly subjective so I may as well make them nice.

The problem is most ways I've seen them implemented are clunky, use images, and hard to maintain. 

Good news is Alfred Genkin posted a nice accessible way to create star reviews and posted it to [CSS-Tricks](https://css-tricks.com/five-methods-for-five-star-ratings/) back before Digital Ocean stopped using the site.

It just uses HTML and CSS, no JavaScript or image shenanigans. It uses the normal Unicode star symbol and applies a gradient over it so you have access to fractional scores. It also uses an aria-label so in theory it is accessible via screen readers and other accessibility tools.

In my Review Template I adapted the code he provided for option 5 in his article:

``` HTML
{{ if .Params.rating }}
    <p>Rating: <span class="Stars" style="--rating: {{.Params.rating}};" aria-label="Rating of this product is {{ .Params.rating }} out of 5."></span></p>
{{ end }}
```

This template checks if the review has a rating parameter in the front matter and if so uses it for the score.

Then there is the CSS taken wholesale from his post:

``` CSS
:root {
    /* --star-size: 60px; */
    --star-color: #fff;
    --star-background: #fc0;
  }
  
.Stars {
    --percent: calc(var(--rating) / 5 * 100%);
    
    display: inline-block;
    font-size: var(--star-size);
    font-family: Times; /* make sure ★ appears correctly */
    line-height: 1;
    
    &::before {
      content: '★★★★★';
      letter-spacing: 3px;
      background: linear-gradient(90deg, var(--star-background) var(--percent), var(--star-color) var(--percent));
      background-clip: text;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
}
```

You can see the results [here](https://techtea.io/reviews/2024/03/yunnan-black-savidsons-organics/). Much easier to get a estimate of how I felt about something. I might use the stars in other places where the review shows up in the future. 

I am not a CSS expert, but this works. In the future I want to theme it to better match with the rest of the site.

Speaking of, I do plan to start work on a custom color scheme that is easier on the eyes soon.
