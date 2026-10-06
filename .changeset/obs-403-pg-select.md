---
'@mastra/pg': minor
---

Added PostgreSQL support for `select` and `include` on trace queries. The store runs a side query only for the fields a request selects, so the output preview, tags, and error preview add no queries at all.
