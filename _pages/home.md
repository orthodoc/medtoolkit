---
layout: landing
title: Home
permalink: /
cta-link: "/courses/get-your-free-guide-on-less-is-more"
problem-title-one: Hate the long working hours?
problem-title-two: Feel empty after a day's work.
agitate-title: It Doesn't have to be that way
solution-title-one: Get back your quality time!
solution-title-two: And extract satisfaction at work.
cta-text: Click here for your free 7-part guide to claiming your time
---
You took the mandatory med courses. You spent quality time diligently following what your teachers taught you. You are not deficient in skills. You were different from your techy friends. You wanted to make an impact in the lives of people.

I am here to say --- *you still can*. But first you have to get rid of that feeling of helplessness. You were born to be a leader. Your patients are looking for you to lead them out of their problems. You *cannot do* that by brushing aside your own problems. Learn to be your true self.

The world has transformed while you were busy pouring yourself over medical books and journals. Its not the industry that drives the world any more. The key word is *information*. [The Third Wave](https://goo.gl/88Kj11) is here. The old medical bag has not only gone out of fashion, but has turned irrelevant. Now we need a different set of tools for the digital world. Come with me on a journey to explore the digital landscape! I have a spanking new toolkit for *you*.

You don't have to tread the lonely path anymore! Welcome.

[Start here.](/courses/get-your-free-guide-on-less-is-more)

---------------------
{% if site.articles[0] %}
#### Articles that may interest you

  <ul>
  {% for article in site.articles limit: 3 %}
    <li>
      <a href="{{ site.baseurl }}{{ article.url }}">
        {{ article.title }}
      </a>
    </li>
  {% endfor %}
{% endif %}
