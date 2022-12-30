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

{% capture temptags %}
  {% for tag in site.tags %}
    {{ tag[1].size | plus: 1000 }}#{{ tag[0] }}#{{ tag[1].size }}
  {% endfor %}
{% endcapture %}
{% assign sortedtemptags = temptags | split:' ' | sort | reverse %}
{% for temptag in sortedtemptags %}
  {% assign tagitems = temptag | split: '#' %}
  {% capture tagname %}{{ tagitems[1] }}{% endcapture %}
  <a href="/tag/{{ tag_name }}"><code class="highligher-rouge" style="color:#969595;border-color:hsla(0, 0%, 59%,0.6)"><nobr>{{ tag_name }}</nobr></code></a>
{% endfor %}


<style>
  .wrapper {
    max-width: 58em;
  }
</style>