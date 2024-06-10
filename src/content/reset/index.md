---
title: Reset
description: set of building blocks and standards that help keep the look and feel of products and experiences consistent.
layout: default
date: 2024-01-03
override:tags: ["primary", "footer"]
---
{% for post in collections.reset %}
- [{{ post.data.title }}]({{ post.url | url }})
{% endfor %}