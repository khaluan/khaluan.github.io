---
layout: page
title: Notes
---

Short notes, grouped by topic. These are working notes rather than blog posts — they get
revised in place instead of being published once.

{% assign topics = site.notes | group_by: "topic" | sort: "name" %}
{% for topic in topics %}
<section class="note-topic">
  <h2 id="{{ topic.name | slugify }}">{{ topic.name }}</h2>
  <ul class="note-list">
    {% assign notes = topic.items | sort_natural: "title" %}
    {% for note in notes %}
    <li>
      <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
      {%- if note.summary %}<span class="note-summary">{{ note.summary }}</span>{% endif -%}
    </li>
    {% endfor %}
  </ul>
</section>
{% endfor %}
