---
date: <% tp.date.now("YYYY-MM-DD") %>
month: <% tp.date.now("YYYY-MM") %>
type: monthly
tags: [monthly, <% tp.date.now("YYYY-MM") %>]
---

# Monthly Summary - <% tp.date.now("MMMM YYYY") %>

## Weekly Reviews
```dataview
LIST FROM "Journal/Weekly"
WHERE type = "week-review" AND month = this.month
SORT date ASC
```

## Key Accomplishments
- 

## Ongoing Work
- 

## Summary
