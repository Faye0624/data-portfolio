# Database design & SQL analytics (PostgreSQL)

Relational schema design and analytical SQL on PostgreSQL.

## What it covers
- **Analytical SQL:** multi-layer CTEs, window functions (ROW_NUMBER / RANK /
  LAG / LEAD with PARTITION BY), recursive CTEs, HAVING, COUNT(DISTINCT), and
  subqueries to answer business-style questions.
- **Schema design & normalization:** model a transactional schema and progress it
  1NF → 3NF → 4NF, analysing functional and multi-valued dependencies to remove
  insertion / update / deletion anomalies.
- **Trade-off analysis:** quantify tuple-level impact across modification
  scenarios to weigh normalization against query efficiency.

## Stack
PostgreSQL, analytical SQL.

## Files
- `database_sql_analytics.pdf` — the write-up.
