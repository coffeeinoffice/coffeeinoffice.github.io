---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Home
permalink: /
order: 1
---

<div class="posts">
  {% for post in site.posts %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">{{ post.date | date_to_string }} | {% include tags.html %}</time>
    

     {{ post.content | markdownify | strip_html | truncatewords: 50 }}
    {% if post.content.size > 50 %}
        <p>
            <br>
            <a href="{{ site.baseurl }}{{ post.url }}">
                Continue reading...
            </a>
            
        </p>
    {% endif %}
  </article>
  {% endfor %}
</div>