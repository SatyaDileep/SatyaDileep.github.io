---
layout: default
title: Blog
---

<style>
.post-list { list-style: none; padding: 0; }
.post-list li { padding: 1rem 0; border-bottom: 1px solid #eee; }
.post-list li:last-child { border-bottom: none; }
.post-list a { font-size: 1.1rem; font-weight: 600; color: #333; text-decoration: none; }
.post-list a:hover { color: #1a73e8; }
.post-list .date { color: #777; font-size: 0.85rem; }
.post-list .desc { color: #555; margin-top: 0.25rem; }
</style>

# Blog

Thoughts on product management, GenAI, agentic automation, and prototyping.

---

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div class="date">{{ post.date | date: "%b %d, %Y" }}</div>
      {% if post.description %}<div class="desc">{{ post.description }}</div>{% endif %}
    </li>
  {% endfor %}
</ul>
