---
title: Grouping with Liquid
topic: Liquid
summary: group_by, and what it hands back
updated: 2021-04-18
---

`group_by` turns a list into groups, each with a `name` (the value grouped on) and
`items` (the documents in it):

{% raw %}    {% assign topics = site.notes | group_by: "topic" %}{% endraw %}

The result is ordered by first appearance, so pipe it through `sort: "name"` for a
predictable page. Documents missing the property collect under an empty name — worth
avoiding with a front matter default.
