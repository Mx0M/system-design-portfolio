# URL Shortener System Design

Welcome to the URL Shortener system design documentation. This directory contains all design artifacts, diagrams, and detailed analyses for a scalable and resilient URL shortener.

## 📘 Index

1. [Requirements & Access Patterns](1-requirements.md)  
   Explains core user and system requirements, latency expectations, and consistency needs.

2. [Capacity Estimates & Metrics](2-capacity-estimation.md)  
   Storage, read/write throughput, and scaling boundaries over time.

3. [High‑Level Design](3-high-level-design.md)  
   Architecture overview, service interaction, async paths, and component breakdown.
   
4. [Low‑Level Design](4-low-level-design.md)  
   Architecture overview, service interaction, async paths, and component breakdown.
   
5. [Database Design](5-database-design.md)  
   Cassandra schema, Redis caching, click counting, and partition strategies.

6. [Scaling Strategy](6-scaling-strategy.md)  
   Node scaling triggers, cache sizing, and service autoscaling suggestions.

7. [Failure Handling](7-failure-handling.md)  
   Retry strategies, fallbacks, and fault tolerance mechanisms.

8. [Major Trade‑offs](8-trade-offs.md)  
   Design decisions table and trade‑off comparisons.

## 📊 Summary

Each file contains detailed explanations, diagrams (if present), and tables for easier understanding. Navigate through the index to explore each aspect of the design.

---
