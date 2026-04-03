# Capacity Estimation

| Metric                | Value     | Calculation                                         |
| --------------------- | --------- | --------------------------------------------------- |
| New URLs per day      | 10M       | 100 writes/sec avg, peak 500 writes/sec             |
| Redirects per day     | 100M      | ~1,160 redirects/sec avg, peak 5,000/sec            |
| Read:write ratio      | 10:1      | Mostly reads (redirects)                            |
| Data per mapping      | 500 bytes | Short code (8B) + long URL (256B) + metadata (236B) |
| New data per day      | 5 GB      | 10M × 500 bytes                                     |
| Total data (10 years) | ~18 TB    | 5GB × 3650 days                                     |
| Cache size            | ~100 GB   | Cache top 20% hottest links                         |

## Notes

- **Short code length**: Use 6 characters (alphanumeric, case-sensitive)
  - Total combinations: 62⁶ ≈ 56 billion possible keys
  - Sufficient capacity for decades
