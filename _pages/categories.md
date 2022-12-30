---
layout: page
permalink: /categories/
title: categories
---

<h1>Categories</h1>

{% for page in site.categories.languages %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}