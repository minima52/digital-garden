---
layout: page
title: archive
permalink: /archive
---

<h1>Archive</h1>

An archive of all the notes in my digital garden sorted by date last modified.

<ul class="archive">
{% for note in site.notes %}
<li><a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">{{note.title}}</a>{% if note.category != null %} in {{note.category}}{% endif %} <span>({{ note.last_modified_at | date: "%B %Y" }})</span></li>
{% endfor %}
</ul>

<h2>All Tags</h2>
{{ site.tags.korean | size }}


<style>
  .wrapper {
    max-width: 58em;
  }
</style>