---
title: Shorts
permalink: "/shorts/"
layout: page
---

<ul class="article-list">
  {% for short in site.shorts %}
    <li>
      <a href="{{ site.baseurl }}{{ short.url }}">
        {{ short.title }}
      </a> <span>•</span>
      {% include reading_time.html %}
    </li>
  {% endfor %}
</ul>
