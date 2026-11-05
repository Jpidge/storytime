---
layout: page
title: "Rowan's Novella"
tags: [rowan, novella, science-fiction]
permalink: /rowans-novella/
---

![Cover art by John T. Page: watercolor close-up of a woman's green eyes amid purple washes — the eyes that started it all]({{ "/assets/Cover%20for%20Rowan's%20novella.webp" | relative_url }}){: .book-cover}

*Cover art: John T. Page, watercolor.*
{: .cover-credit}

<div class="post-tags book-tags">{% for tag in page.tags %}<a class="post-tag" href="{{ '/tags/' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% endfor %}</div>

An intimate story of love and irreversibility — what a person is, when she cannot be copied, restored, or testified for. Chapters post here as they are finalized: critiqued, revised, and merged.

{% assign posts = site.categories["rowans-novella"] %}
{% if posts.size > 0 %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
{% else %}
*The first chapter is in the workshop. It will appear here the moment it is final.*
{% endif %}

[RSS feed for this book]({{ '/rowans-novella/feed.xml' | relative_url }}) · [Back to the library]({{ '/' | relative_url }})
