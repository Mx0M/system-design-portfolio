# Summary Table of Major Trade-offs

| Area            | Trade-off A          | Trade-off B                | Winner at scale |
| --------------- | -------------------- | -------------------------- | --------------- |
| Database        | SQL (simple)         | NoSQL (scalable)           | NoSQL           |
| Code generation | Random (privacy)     | Sequential (simple)        | Random          |
| Uniqueness      | Optimistic (fast)    | Pessimistic (safe)         | Pessimistic     |
| Caching         | Cache‑aside (simple) | Write‑through (consistent) | Cache‑aside     |
| Click counting  | Sync (accurate)      | Async (scalable)           | Async           |
| Expiration      | Native TTL           | Background cleanup         | Native TTL      |
| Redirect status | 301 (cached)         | 302 (controllable)         | Hybrid          |
