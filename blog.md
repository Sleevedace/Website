---
layout: default
title: Blog
permalink: /blog/
---

# Blog

{% for post in site.posts %}
<article class="blog-post">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
  <p>
    {% for tag in post.tags %}
      <a href="/tags/#{{ tag }}" class="tag">{{ tag }}</a>
    {% endfor %}
  </p>
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %}
