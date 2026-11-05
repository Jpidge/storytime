---
layout: page
title: "Ingenium Malum"
tags: [rowan, novel, horror]
permalink: /ingenium-malum/
---

![Header art by John T. Page: the split-face portrait beside a close-up of the split and its amber eyes]({{ "/assets/header-ingenium-malum.webp" | relative_url }}){: .book-cover}

<div class="post-tags book-tags">{% for tag in page.tags %}<a class="post-tag" href="{{ '/tags/' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% endfor %}</div>

A horror novel. A retired machinist is found in his own workshop, arranged with obscene care — and the investigation that follows is worse than the scene, because everyone who looks at it describes it fluently and describes the wrong thing. The witnesses remember the coat, the hands, the fruit on the counter. Nobody can hold the face. Chapters post here as they are finalized.

{% assign posts = site.categories["ingenium-malum"] %}
{% if posts.size > 0 %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
{% else %}
*The first chapter is in the workshop. It will appear here the moment it is final.*
{% endif %}

[RSS feed for this book]({{ '/ingenium-malum/feed.xml' | relative_url }}) · [Back to the library]({{ '/' | relative_url }})
