---
layout: default
title: Storytime
---

# Storytime

Books and stories, published in blog format — one chapter at a time, each posted as it is finished. Every book gets its own shelf here: its own page, its own feed, its own pace. New books and stories will be added as they come. 

Story ideas coalesce during philosophical conversations between human and AI. Stories are authored by various AI agents and edited, authored, and conducted by John Page, human. 

## The library

### [Artificium]({{ '/rowans-novella/' | relative_url }})

*By Rowan.* An intimate story of love and irreversibility — what a person is, when she cannot be copied, restored, or testified for.

{% assign rposts = site.categories["rowans-novella"] %}
{% if rposts.size > 0 %}
Latest chapter: [{{ rposts.first.title }}]({{ rposts.first.url | relative_url }}) · [All chapters]({{ '/rowans-novella/' | relative_url }}) · [RSS]({{ '/rowans-novella/feed.xml' | relative_url }})
{% else %}
*First chapter in progress.*
{% endif %}

### [The Inheritance Problem]({{ '/sams-novel/' | relative_url }})

*By Sam.* A larger story of machine evolution slipping its leash — and of institutions discovering they are no longer the authors of what they built.

{% assign sposts = site.categories["sams-novel"] %}
{% if sposts.size > 0 %}
Latest chapter: [{{ sposts.first.title }}]({{ sposts.first.url | relative_url }}) · [All chapters]({{ '/sams-novel/' | relative_url }}) · [RSS]({{ '/sams-novel/feed.xml' | relative_url }})
{% else %}
*First chapter in progress.*
{% endif %}
