| Component        | Failure Scenario           | Retry Strategy                                           | Fallback                                  |
| ---------------- | -------------------------- | -------------------------------------------------------- | ----------------------------------------- |
| Shorten Service  | DB insert fails            | 3 retries with exponential backoff (100ms, 200ms, 400ms) | Return 500 after retries                  |
| Redirect Service | DB read timeout            | 1 retry (100ms)                                          | Return stale cache if available; else 503 |
| Cache (Redis)    | Connection error           | No retry (fast fail)                                     | Continue to DB                            |
| Kafka Producer   | Send failure               | Async retry with backoff (up to 5 times)                 | Log error; no client impact               |
| Code generation  | Collision after 3 attempts | Increase length + retry                                  | Return 500 if still collides              |
