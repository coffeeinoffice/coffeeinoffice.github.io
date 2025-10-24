---
layout: post
title: "Using GitHub Repository for Note Taking"
date: 2025-10-22 22:41:26 +0200
tags: [Github, Productivity, Markdown]
---

I'm a nerd, at least somehow. Since years I'm always looking to improve stuff and use tools to make my life easier. One of my biggest topics I still struggle with is a proper note taking and organizing system. I tried nearly everything. Started with Apple Notes, moved to Evernote, moved to Notion, took a look at Obsidian, moved back to Apple Notes. And it never ends. The biggest issues I had on this journey are:

1. Access notes from everywhere on every device is not smooth.
2. Dealing with tool settings, formatting, etc. instead of taking and organizing notes.
3. Vendor lock-in drives me crazy with their changes where I have to adopt my workflow.

Both of these topics are still driving me crazy and I still try to figure out a good method and compromise. Let me explain some of these issues and a potential solution I'm currently trying.

## Access notes from everywhere

Yes, all mentioned tools are somewhat promoting themselves as tools that are available everywhere and across platforms. This is somewhat true, but there is always a downside coming with this.

**Apple Notes**

As fan of Apple Products this was my favorite note taking tool and I always jump back to this when all other options are no longer working for me. When working in the Apple device environment this is all fine, sometimes the mobile app usage is a little strange but it works with synchronization etc. like a charm. But... I want to take notes and replace my offline notebook which I also use for some work related stuff, where I'm supposed to use Windows and no Apple device.

_Did you ever try working with Apple Notes on a Windows Device, or better in the browser?_

I hope you never had to use it. Everything that runs so smooth on the Apple devices with inserting screenshots, creating links etc. is just not usable on the browser/windows side. And this is the biggest issue I have when we look at cross device usage of a notes app.

**All others**

They work all very well because they are designed to use in a browser and don't really require an app. Of course you can use the apps which makes the user experience better, especially on mobile devices but you don't have. Different to Apple Notes the functionality works everywhere the same.

## Dealing with tool settings, formatting, etc.

Even though I'm a nerd that tries various software solutions I still hate setting up tool settings. This drives me crazy what I have to do, especially when it comes down to data privacy. And after the settings are done you have to check them again after each upgrade because there might be changes come like "Allow AI to learn from your data", which sounds somewhat nice but who else will have access to this or gets generated data out of my notes?

If you dealt with all the settings in your tools, you can start creating and writing your notes. Hit your buttons and let the flow begin. Very soon you identify that you will stop typing and start editing what you have written. This includes building headlines or lists or mark things **bold** or _italic_. All this takes time away from your notes and writing process. And I get that why we are all doing this, we need structure in our notes and formatting helps, but it stops the writing flow if you deal with it in between. And this is unfortunately what happens, even when you tell your brain to wait with formatting until everything is done and written. There are some "boring" moments in a meeting where everyone will for sure start working on the formatting.

## Vendor lock-in

This is my favorite topic and very hard to avoid or argue with. I usually don't have an issue to get into a vendor lock-in if the vendor is some kind of a global player where I can trust that they will not shut down stuff soon, or am I wrong if we look at Microsoft with Microsoft Project Online? ;-)

In addition to the shut down, a vendor lock-in always has the risk that some functionality of your workflow will no longer be available or that features are release that you don't want but can't deactivate. If this happens you have difficulties with most vendors to get your data out of their system in an easy way which is a potential risk to loose everything you have done.

Anyhow, I was looking for an option that solves my issues #1 and #2 and ideally I can deal also with issue #3 with a new setup.

## My current idea is to use GitHub and Markdown

Since I'm working in IT and I like dealing with coding and technology I wanted to explore a more none-fancy tool way. Some of you might be familiar with GitHub and Markdown and some not. Don't worry I will not try to explain in depth what each of these words mean but I try to give you an idea, how these two "tools" could help me with my three issues.

Here is a quick explanation of both "tools":

GitHub
: In GitHub you can create so called "Repositories" that story any kind of information. Usually this is used within software engineers or developers to create and collaborate on code and have version control for their changes directly built into the tool. Fun fact, this blog is hosted on GitHub as well.

Markdown
: Markdown is a lightweight markup language that you can use to add formatting elements to plaintext text documents. This means that you can just write text and use e.g. ** to make something **bold**. Same works for headings, etc.

### Issue 1 - Access notes from everywhere

All repositories you create on Github are accessible everywhere, independent of operating system, browser or mobile devices. This is an awesome feature and it comes totall for free.

So my idea is to setup a private notes repository where I will store all my notes in markdown files. Markdown files can be edited either directly on GitHub or with any note editor or with your prefered IDE where you can ideally use git commands as well to sync your changes.

I don't know yet if this will work but at least issue #1 is solved with Github and Markdown files.

### Issue 2 - Dealing with tool settings

Neither Github nor markdown require any specific tool settings. You can setup a user account on Github (any developer probably has it anyhow) and create a private repository with some minimal setting if needed.

For markdown files you just need any text editor or use the built in from GitHub. You can save all files as .md or .markdown and you are done.

### Issue 3 - Vendor lock-in

Github is some kind of a vendor lock-in. It works like a charm to synchronize your repositories, etc. but it is all based on open source git. So if Github will be no longer available or changes features you would be able to move to some other platform that works similar, e.g. Gitlab or you try to setup a platform on your own.

Markdown itself is totally independent, at least if you use the default syntax. If you choose to use special variants from the syntax you might have issues with some interpreters but if not you can move your markdown files anyhwere and have it previewed in a lot of editors and websites.

## Conculision

I will keep you posted on how my experience is going and how my setup looks like in my notes repository. I'm not sure if this will be the final note taking system for me but it look promising so far.

Stay tuned and enjoy your coffee!