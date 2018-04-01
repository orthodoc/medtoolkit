---
title: Articles
permalink: "/"
layout: page
---

<ul class="article-list">
  {% for article in site.articles %}
    <li>
      <a href="{{ site.baseurl }}{{ article.url }}">
        {{ article.title }}
      </a> <span>•</span>
      {% include reading_time.html %}
    </li>
  {% endfor %}
</ul>
