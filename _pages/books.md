---
title: Books
permalink: "/books/"
layout: page
---

<ul class="article-list">
  {% for book in site.books %}
    <li>
      <a href="{{ site.baseurl }}{{ book.url }}">
        {{ book.title }}
      </a>
    </li>
  {% endfor %}
</ul>
