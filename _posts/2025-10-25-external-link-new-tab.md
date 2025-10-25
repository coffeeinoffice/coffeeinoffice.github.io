---
title: "Open external links in new tab automatically in Markdown posts"
tags: [Markdown, "Blog Setup"]
---

Is there anything worse when you're reading a blog or article on the web and there are links pointing to other information or tools or whatever and if you click on them they load in your current tab? I really hate this behavior because I like that I get pointed to a further analysis or a helpful tool but still want to read that article.

Since I started blogging years ago I always ensured that my external links are opening in a different tab or window. Back in these days I was using Wordpress for my blogs and probably also some plugin to handle external links. Now I have a totally new setup that I have to learn and figure out how things work. In this article you will learn how you can achieve this with default functionalit of Jekyll.

## Markdown and external links

When I first started writing stuff in Markdown I was impressed how fast I can write a new article and I don't have to worry about formatting, etc. Then I started digging deeper, using To-Do's, Mermaid, and of course links in my notes and articles. All of this is very easy to use and I really like that behavior to focus on the content you write instead of anything else.

Now I started blogging with Markdown articles and realized it is somehow not possible to open external links in a new tab. There is just no syntax for that option. I tried to figure out how I could achieve this and there are a lot of options. One of them is to extend the links via the Markdown text because Jekyll is using [Kramdown](https://kramdown.gettalong.org), a variation of Markdown, which lets you add an extension to a link that will then open in a new tab.

To achieve that all you have to do is to add something like this behind your links:
```md
[link](url){:target="_blank"}
```

So this works very well with the blog setup I have but it is not everything I wanted to add to my links. From a SEO and crawler perspective I wanted to add also other attributes like **nofollow**, **noopener**, **noreferrer** to my links. I moved on and looked for a different solution, not only because of the missing attributes but also because remembering to add this to all external links was just something I knew I will forget soon.

## Jekyll Plugin and GitHub

As you know from my [first post](/posts/new-setup-with-github-pages/) about this blog I host my blog via Github pages, which btw. works awesome. Besides the hosting I also use Jekyll als markdown translater and page creator for this website, which also works awesome. And now Jekyll is offering various plugins to add stuff to external links or you could also write your own plugins if you want to, but...

There is always a but... Github is very restrictive when it comes to plugins or ruby gems and most of the plugins that solve that link topic are not supported, so that was not a solution either.

## My solution using pure Liquid functionality

It took some time to find another option until I found a function in the liquid logic within Jekyll. Voila, there is a functionality called [Replace]((https://shopify.github.io/liquid/filters/replace/)) that I just figured out on how to use it to my favor.

I now added to one of my layouts where my post content gets created the following part:

{%raw%}
```
{{ content | replace: '<a href="http', '<a rel="nofollow noopener noreferrer" target="_blank" href="http' }}
```
{%endraw%}

With this addition to the content variable I look for links that start with "http" because I assume that these are external links. Links within my blog are usually indirect links so this replace will not work. And if this is the case the replace function replaces the created html for links from my markdown and addes the seo attributes as well as the target="_blank" to it.

And this works like a charm. Of course it has some assumptions how external links look like but for my requirements it was a very good fit.

_How do you solve these kind of things?_