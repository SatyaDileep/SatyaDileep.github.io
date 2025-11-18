---
layout: default
title: Blog
---

<section class="grid">
  <h2 class="section-title">Blog Posts</h2>

  <ul>
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> – {{ post.date | date: "%b %d, %Y" }}
      </li>
    {% endfor %}
  </ul>
</section>
