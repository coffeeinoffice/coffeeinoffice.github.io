---
layout: post
title: "Add icons to external links via CSS"
date: 2025-10-24 18:41:26 +0200
tags: ["Blog Setup"]
---

If you are like me and you are browsing any kind of blog or website to learn and figure out how things work, you probably come across links to pages different then the current url. You would assume that these links are opening a new tab so you can read the reference after you finished reading the current page, but often this is not the case and the links open directly in the current tab.

I wanted to avoid this so I setup a general logic in my Jekyll blog via the [Liquid Replace](/404.html) functionality. But just having the links open in a new tab was not enough for me, I wanted to also make it visible that the links are pointing to an external site.

## Using CSS to add an icon to external links
There are multiple options how you can add an icon to an external link. There are Jekyll plugins, you can use javascript or like I did, use CSS. I preferred the simple CSS way because I host my website via Github pages which do not support many Jekyll plugins. I also decided against javascript because there are still users who have this deactivated. 

To setup the icons to external links I prefer to use a SVG image. You can modify links via the :after method in CSS. As example on how this looks on my page:

{% include codeHeader.html %}
```css
a:not(
      [href^="#"],
      [href^="/"],
      [href*="localhost"],
      [href*="coffeeinoffice.com"]
    )::after {
    content: "";
    width: 11px;
    height: 11px;
    margin-left: 3px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' fill='%23ff0f00' viewBox='0 0 16 16'%3E%3Cpath fill-rule='evenodd' d='M8.636 3.5a.5.5 0 0 0-.5-.5H1.5A1.5 1.5 0 0 0 0 4.5v10A1.5 1.5 0 0 0 1.5 16h10a1.5 1.5 0 0 0 1.5-1.5V7.864a.5.5 0 0 0-1 0V14.5a.5.5 0 0 1-.5.5h-10a.5.5 0 0 1-.5-.5v-10a.5.5 0 0 1 .5-.5h6.636a.5.5 0 0 0 .5-.5z'/%3E%3Cpath fill-rule='evenodd' d='M16 .5a.5.5 0 0 0-.5-.5h-5a.5.5 0 0 0 0 1h3.793L6.146 9.146a.5.5 0 1 0 .708.708L15 1.707V5.5a.5.5 0 0 0 1 0v-5z'/%3E%3C/svg%3E");
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
    display: inline-block;
  }
```

With the first part, we exclude which kind of links should not have the icon added. I just want to add the icon in my case to external links not to links within the same page / url.

```css
a:not(
      [href^="#"],
      [href^="/"],
      [href*="localhost"],
      [href*="coffeeinoffice.com"]
```

The second part is used to show the icon behind the link. This is a encoded svg image as you can see. You can use whatever you want as an svg code, I just like the default that is seen on most websites. If you want to change the color of the icon like I did to a hex code you can do so in the url string with a **"%23000000"** instead of **"#000000"**.

```css
::after {
    content: "";
    width: 11px;
    height: 11px;
    margin-left: 3px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' fill='%23ff0f00' viewBox='0 0 16 16'%3E%3Cpath fill-rule='evenodd' d='M8.636 3.5a.5.5 0 0 0-.5-.5H1.5A1.5 1.5 0 0 0 0 4.5v10A1.5 1.5 0 0 0 1.5 16h10a1.5 1.5 0 0 0 1.5-1.5V7.864a.5.5 0 0 0-1 0V14.5a.5.5 0 0 1-.5.5h-10a.5.5 0 0 1-.5-.5v-10a.5.5 0 0 1 .5-.5h6.636a.5.5 0 0 0 .5-.5z'/%3E%3Cpath fill-rule='evenodd' d='M16 .5a.5.5 0 0 0-.5-.5h-5a.5.5 0 0 0 0 1h3.793L6.146 9.146a.5.5 0 1 0 .708.708L15 1.707V5.5a.5.5 0 0 0 1 0v-5z'/%3E%3C/svg%3E");
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
    display: inline-block;
  }
```