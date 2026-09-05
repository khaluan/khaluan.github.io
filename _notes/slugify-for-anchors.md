---
title: slugify for anchors
topic: Liquid
summary: Making a heading linkable from elsewhere
updated: 2021-04-18
---

`slugify` lowercases a string and replaces anything awkward with hyphens, so the same
filter applied on both ends produces a link that matches its target:

{% raw %}    <h2 id="{{ topic.name | slugify }}">{{ topic.name }}</h2>{% endraw %}

Kramdown already generates ids for headings in Markdown content, but headings built in
a layout or a Liquid loop need theirs set explicitly.
