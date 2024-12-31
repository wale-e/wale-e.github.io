---
layout: default
title: "Home"
---

# Welcome to the Ai Agentic World

I write about **Ai Agent** *frameworks* and *platforms*.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — *{{ post.date | date_to_string }}*
{% endfor %}