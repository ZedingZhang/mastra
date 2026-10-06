---
'@mastra/core': minor
---

Added `select` and `include` to advanced trace queries, so a Traces table gets the columns it shows from one request and pays only for those columns.

```typescript
{
  timeRange,
  select: ['outputPreview', 'errorPreview', 'errorCounts'],
  include: { scores: true },
  page: { limit: 25 },
}
```

`select` accepts `outputPreview`, `tags`, `errorPreview`, `errorCounts`, `model`, `timeToFirstTokenMs`, `promptCacheReadTokens`, and `promptCacheCreationTokens`. `include.scores` adds one average per scorer. Each row carries only the keys you asked for.
