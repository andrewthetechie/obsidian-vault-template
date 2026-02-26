---
date: <% tp.date.now("YYYY-MM-DD") %>
week: <% tp.date.now("YYYY-[W]WW") %>
month: <% tp.date.now("YYYY-MM") %>
type: week-review
tags: [weekly, review, <% tp.date.now("YYYY-MM") %>]
---

# Week in Review - <% tp.date.now("YYYY-[W]WW") %>

## Daily Notes
```dataview
LIST FROM "Journal/Daily"
WHERE date >= date(this.date) - dur(6 days) AND date <= date(this.date)
SORT date ASC
```

## Accomplishments
- 

## Carried Over
- 

## How the Week Went
