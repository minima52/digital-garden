---
layout: page
permalink: /categories/
title: categories
---

<h1>Categories</h1>

        <div class="post-categories">
          {% if post %}
            {% assign categories = post.categories %}
          {% else %}
            {% assign categories = page.categories %}
          {% endif %}
          {% for category in categories %}
          Categories: <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
          {% unless forloop.last %}&nbsp;{% endunless %}
          {% endfor %}
        </div>