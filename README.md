# Real-Time Change Data Capture (CDC) Lakehouse

**Debezium → Kafka → Spark Structured Streaming → Delta Lake (MinIO) → dbt (Snowflake optional)**

## What this repo will have
- Docker Compose stack for Postgres + Debezium (Kafka Connect) + Kafka + Schema Registry + Spark + MinIO
- Example OLTP schema (8+ tables) with CDC enabled (logical decoding)
- Spark streaming job writing to Delta Lake with checkpoints & watermarks
- Data contracts via Schema Registry + basic Great Expectations checks
- dbt models (incremental + SCD Type-2) for analytics

## Quick start (coming soon)
1) copy `.env.example` → `.env` and fill values  
2) `docker compose up -d`  
3) open Spark UI / Kafka UI, verify topics & streams  
4) run dbt to materialize warehouse tables (optional Snowflake)

## Status
Step 1: ✅ repo created

## License
MIT
