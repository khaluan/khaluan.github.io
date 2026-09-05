---
layout: post
title: A Small Toolbox for Repeated Work
author: Alex Morgan
tags: [Technology, Tools, Notes]
---

Repeated work gets easier when the useful parts are named. These are a few patterns I reach for when a task starts appearing for the third time.

## Start with a query

When the data is unclear, a small query is often more helpful than a large abstraction.

```tsql
SELECT TOP 10
    p.name AS ProjectName,
    COUNT(t.id) AS TaskCount
FROM dbo.Projects AS p
LEFT JOIN dbo.Tasks AS t ON t.project_id = p.id
GROUP BY p.name
ORDER BY TaskCount DESC;
```

## Automate the boring edge

The first automation does not need to own the whole workflow. It can simply make the next command harder to forget.

```powershell
$posts = Get-ChildItem "_posts" -Filter "*.md"

foreach ($post in $posts) {
    Write-Output "Checking $($post.Name)"
}
```

## Leave a useful failure

Good tools make the happy path quick and the unhappy path legible. A clear message, a small output file, or a link to the relevant note can save more time than another clever helper function.

The toolbox stays small on purpose. Every addition should remove friction from a real, repeated task.