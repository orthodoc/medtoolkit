---
layout: page
title:
permalink: /books/
---
{% if site.books[0] %}
<h3 class="post-title">Books</h3>

<ul class="article-list">
  {% for book in site.books %}
    <li>
      <a href="{{ site.baseurl }}{{ book.url }}">
        {{ book.title }}
      </a>
    </li>
  {% endfor %}
</ul>
{% else %}
<h3 class="post-title">Books</h3>
  {% for book in site.books %}
    {% unless book.published %}
      {% capture count %}{{ count | plus: 1 }}{% endcapture %}
    {% endunless %}
  {% endfor %}
  {{ count }} books are being dusted and prepared for the site. Come back later to check them out here.
{% endif %}
