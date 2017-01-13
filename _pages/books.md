---
layout: page
title: Books
permalink: /books/
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
