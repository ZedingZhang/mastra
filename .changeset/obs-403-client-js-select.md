---
'@mastra/client-js': minor
---

`queryTraces()` accepts `select` and `include` to add fields such as the output preview, the error that ended the run, error counts, and per-scorer averages to every trace row.

```typescript
const result = await mastraClient.queryTraces({
  timeRange,
  select: ['outputPreview', 'errorPreview'],
  page: { limit: 25 },
})
result.traces[0].errorPreview // 'AI_APICallError: The model `gpt-5` does not exist.'
```
