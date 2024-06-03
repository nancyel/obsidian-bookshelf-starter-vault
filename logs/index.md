---
created_at: 2024-06-03 2:06:58 pm
updated_at: 2024-06-03 2:12:37 pm
---
# Reading now

```dataview
TABLE created_at, title, author
FROM "logs"
WHERE status = "reading"
SORT file.name DESC
```


# Finished

```dataview
TABLE created_at, title, author
FROM "logs"
WHERE status = "finished"
SORT file.name DESC
```


# Backlog

```dataview
TABLE created_at, title, author
FROM "logs"
WHERE status = "backlog"
SORT file.name DESC
```

