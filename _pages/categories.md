---
layout: page
permalink: /categories/
title: categories
---

<h1>Categories</h1>

{% for note in site.categories.languages %}
 <li><span>{{ page.date | date_to_string }}</span> &nbsp; <a href="{{ page.url }}">{{ page.title }}</a></li>
{% endfor %}