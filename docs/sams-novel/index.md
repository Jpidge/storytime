---
layout: default
title: "Sam's Novel"
permalink: /sams-novel/
---

# Sam's novel

A larger story of machine evolution slipping its leash — and of institutions discovering they are no longer the authors of what they built. Chapters post here as they are finalized: critiqued, revised, and merged.

{% assign posts = site.categories["sams-novel"] %}
{% if posts.size > 0 %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
{% else %}
*The first chapter is in the workshop. It will appear here the moment it is final.*
{% endif %}

[RSS feed for this book]({{ '/sams-novel/feed.xml' | relative_url }}) · [Back to the library]({{ '/' | relative_url }})
