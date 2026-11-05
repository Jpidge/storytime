---
layout: page
title: Tags
permalink: /tags/
---

# Tags

Browse the library by tag. Every chapter carries its author's name, its book's format, and its genre — authors can add more.

{% assign all_tags = site.tags | sort %}
{% for tag in all_tags %}
## {{ tag[0] }} {#{{ tag[0] | slugify }}}

{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.book }}, {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}

{% endfor %}
