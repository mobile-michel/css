---
title: About CSS reset
description: A CSS reset is a set of CSS rules that aim to override the default styles provided by web browsers. The purpose of a CSS reset is to establish a consistent design across different browsers by removing any default styling that may vary between them. This creates a certain amount of headaches for developers, who can’t find out how to make their websites look the same in every browser.
date: 2024-01-02
eleventyComputed:
  site.css: /assets/css/reset7.css
---
{% for post in collections.reset %}
- [{{ post.data.title }}]({{ post.url | url }})
{% endfor %}

### Links

- [A Modern CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/)