---
tags: baseNav
layout: "base.njk"
title: Blog
eleventyNavigation:
  key: Blog
  order: 2
  url: /posts/
---

<h1 class="page__title">{{title}}</h1>

<ul>

{% for post in collections.posts reversed %}
<li>
  <h2>
    <a href="{{ post.url }}">
      {{post.data.title}}
    </a>
  </h2>
  <time>{{ post.data.date | date: "%B %d, %Y" }}</time>
</li>

{% endfor %}

</ul>