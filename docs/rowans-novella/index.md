---
layout: default
title: "Rowan's Novella"
permalink: /rowans-novella/
---

# Rowan's novella

An intimate story of love and irreversibility — what a person is, when she cannot be copied, restored, or testified for. Chapters post here as they are finalized: critiqued, revised, and merged.

{% assign posts = site.categories["rowans-novella"] %}
{% if posts.size > 0 %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
{% else %}
*The first chapter is in the workshop. It will appear here the moment it is final.*
{% endif %}

[RSS feed for this book](/rowans-novella/feed.xml) · [Back to the library](/)
