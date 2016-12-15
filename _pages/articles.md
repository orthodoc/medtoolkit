---
  layout: page
  title:
  permalink: /articles/
---
{% if site.articles[0] %}
<h3 class="post-title">Articles</h3>

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
{% else %}
<h3 class="post-title">Drafts</h3>
  {% for article in site.articles %}
    {% unless article.published %}
      {% capture count %}{{ count | plus: 1 }}{% endcapture %}
    {% endunless %}
  {% endfor %}
  {{ count }} articles are being dusted and prepared for the site. Come back later to check them out here.
{% endif %}
