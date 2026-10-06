---
'@mastra/server': minor
---

`POST /observability/traces/query` accepts `select` and `include` and adds the requested fields to every trace row. Stores that don't support them return a structured `501`.
