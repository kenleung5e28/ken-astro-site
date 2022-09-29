---
title: "Upsert in Sqlite"
date: "2020-06-28"
draft: false
tags:
- sql
---

From the [official documentation of Sqlite](https://www.sqlite.org/lang_UPSERT.html "upsert"):
> "UPSERT is a special syntax addition to INSERT that causes the INSERT to behave as an UPDATE or a no-op if the INSERT would violate a uniqueness constraint."

Example:

```sql
INSERT INTO Employees(id, name) VALUES (1, "John") ON CONFLICT(id) DO UPDATE SET name = excluded.name
```

The effect is inserting a row `(1, John)` if there is no rows with `id = 1`, or otherwise update the `name` field of the row with `id = 1` to `John`.