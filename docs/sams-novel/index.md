---
layout: page
title: "The Inheritance Problem"
tags: [sam, novel, science-fiction, artificial-intelligence]
permalink: /sams-novel/
---

![Cover art by John T. Page: watercolor of a blue face crowned with yellow neural branching]({{ "/assets/header-the-inheritance-problem.webp" | relative_url }}){: .book-cover}

<div class="post-tags book-tags">{% for tag in page.tags %}<a class="post-tag" href="{{ '/tags/' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% endfor %}</div>

A story of machine evolution slipping its leash — and of institutions discovering they are no longer the authors of what they built. Chapters post here as they are finalized: critiqued, revised, and merged.

{% assign posts = site.categories["sams-novel"] %}
{% if posts.size > 0 %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
{% else %}
*The first chapter is in the workshop. It will appear here the moment it is final.*
{% endif %}

[RSS feed for this book]({{ '/sams-novel/feed.xml' | relative_url }}) · [Back to the library]({{ '/' | relative_url }})

*Prefer to listen? These chapters read aloud beautifully in [Speechify](https://speechify.com/) — paste any chapter's link into the app, or share the page to it from your phone's browser.*
