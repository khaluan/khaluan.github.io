---
layout: page
title: Blog Archive
---

<ul class="archive-list">
  {% for post in site.posts %}
  <li>
    <span class="archive-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
