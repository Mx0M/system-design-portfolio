# 1. Core Requirements & Access Patterns

| Pattern                             | Volume   | Latency          | Consistency                     |
| ----------------------------------- | -------- | ---------------- | ------------------------------- |
| SELECT by short_code (redirect)     | 100M/day | < 5ms p99        | Strong (or eventual with cache) |
| INSERT new mapping (shorten)        | 10M/day  | < 20ms           | Strong (avoid duplicate codes)  |
| UPDATE click count                  | 100M/day | async (eventual) | Counter increments              |
| SELECT by user_id (list user links) | 1M/day   | < 50ms           | Strong / read-after-write       |

---

# 2. Database Choice: Cassandra (with Redis cache)

## Why Cassandra?

- Linear write scalability  
  _(10M inserts/day → 115 writes/sec avg, 500 peak – easy)_
- Multi-region active‑active replication (high availability)
- No single point of failure
- Handles counter columns for click counts
- Tunable consistency (speed vs. accuracy)

## Why not PostgreSQL?

- Works for < 100M total rows, but at 1B+ rows, sharding becomes manual
- Cassandra offers **automatic partitioning** + **zero downtime scaling**
