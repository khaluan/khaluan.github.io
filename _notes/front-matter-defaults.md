---
title: Front matter defaults
topic: Jekyll
summary: Set a value once instead of in every file
updated: 2021-04-11
---

Anything repeated in every file's front matter can move into `defaults:` in `_config.yml`.
Scope it by `path` and `type`, and a document that sets the value itself still wins.

This is how every note in this collection gets `layout: note` without saying so, and how
a note with no `topic` still lands in a group instead of disappearing.
