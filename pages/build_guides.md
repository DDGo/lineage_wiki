---
title: Build guides
sidebar: home_sidebar
permalink: build_guides.html
---

{% assign sorted_pages = (site.pages | sort: 'title') %}

{% for page in sorted_pages %}
{% if page.title and page.url and page.url contains "/devices/" and page.url contains "/build" %}
- [{{page.title}}]({{ page.url | relative_url }})
{% endif %}
{% endfor %}
