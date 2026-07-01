---
layout: default
title: Home
---

# Lacey's Notes

Relatable, evidence-aware reflections on therapy concepts in daily life.

## Recent Posts

{% for post in site.posts limit: 10 %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
