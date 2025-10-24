---
layout: default
title: Tags
permalink: /tags-missing
---

{%- assign post_tags = site.post_tags | map: "title" -%}
{%- for tag in site.tags -%}
    {%- if post_tags contains tag[0] -%}
    {% else %}
- {{ tag[0] }}
    {%- endif -%}
{%- endfor -%}
