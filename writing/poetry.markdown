---
layout: page
title: poetry
nav: false
permalink: /writing/poetry/
categories: poetry
---

<ul class="list list--posts">
  {% for post in site.categories[page.category] %}
    <li class="item item--post">
      <article class="article article--post typeset">
        <h2>
          <a href="{{ site.baseurl }}{{ post.url }}">
            {{ post.title }}
          </a>
        </h2>

        {% include post-meta.html %}

        {{ post.excerpt | markdownify | truncatewords: 60 }}
      </article>
    </li>
  {% endfor %}
</ul>
