# URL Shortener System Design

Welcome to the URL Shortener system design documentation. This directory contains all design artifacts, diagrams, and detailed analyses for a scalable and resilient URL shortener.

## 📘 Index

1. [Requirements & Access Patterns](requirements.md)  
   Explains core user and system requirements, latency expectations, and consistency needs.

2. [Capacity Estimates & Metrics](metrics.md)  
   Storage, read/write throughput, and scaling boundaries over time.

3. [High‑Level & Low‑Level Design](architecture.md)  
   Architecture overview, service interaction, async paths, and component breakdown.

4. [Database Design](db.md)  
   Cassandra schema, Redis caching, click counting, and partition strategies.

5. [Scaling Strategy](scaling.md)  
   Node scaling triggers, cache sizing, and service autoscaling suggestions.

6. [Failure Handling](failure.md)  
   Retry strategies, fallbacks, and fault tolerance mechanisms.

7. [Major Trade‑offs](tradeoffs.md)  
   Design decisions table and trade‑off comparisons.

## 📊 Summary

Each file contains detailed explanations, diagrams (if present), and tables for easier understanding. Navigate through the index to explore each aspect of the design.

---
