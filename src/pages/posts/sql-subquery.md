---
title: "SQL Subquery"
date: "2020-06-17"
draft: false
tags:
- sql
---

Suppose there are two tables `A (id, b_id, value)` and `B (id, item)`, where the column `b_id` is a foreign key referencing table `B` and null is allowed. To query for all rows in the form of `(id, value, item)`, one can use subquery as below.

```sql
SELECT id, value, (SELECT item FROM B WHERE id = b_id) item FROM A
```