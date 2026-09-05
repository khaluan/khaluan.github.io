---
title: Collections vs. posts
topic: Jekyll
summary: When a page is not really a blog entry
updated: 2021-04-05
---

Posts are dated and ordered; collections are not. A note that gets revised in place
belongs in a collection, because its useful metadata is its topic, not its publication date.

A collection needs two things in `_config.yml`: an entry under `collections:` with
`output: true` so each document gets its own page, and a `permalink` if the default
`/:collection/:path/` is not what you want.
