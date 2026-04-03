| Metric                    | Value                                                                               |
| ------------------------- | ----------------------------------------------------------------------------------- |
| Total mappings (10 years) | 36.5B rows (10M/day × 365 × 10)                                                     |
| Raw storage (with RF=3)   | ~55 TB (url_mappings) + ~5 TB (clicks) + 33 TB (user view)                          |
| Read throughput           | 1,150 reads/sec avg, 5,000 peak                                                     |
| Write throughput          | 115 writes/sec avg, 500 peak                                                        |
| Scaling                   | Add nodes when CPU > 70% or storage > 80%. Cassandra automatically rebalances data. |
