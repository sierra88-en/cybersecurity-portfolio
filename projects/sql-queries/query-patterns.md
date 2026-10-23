# SQL Query Patterns: Safe Filtering and Analysis

- **Database/engine:** [SQLite / PostgreSQL / MySQL and version]
- **Dataset:** Synthetic only — [describe generator/source]
- **Objective:** Demonstrate explicit filtering, aggregation, and safe query construction.

## Synthetic schema

```sql
CREATE TABLE lab_events (
    event_id INTEGER PRIMARY KEY,
    event_type TEXT NOT NULL,
    severity TEXT NOT NULL,
    created_at TEXT NOT NULL,
    source_label TEXT NOT NULL
);
```

## Defensive query examples

Select only needed fields and constrain the time range:

```sql
SELECT event_id, event_type, severity, created_at
FROM lab_events
WHERE created_at >= :start_time
  AND created_at < :end_time
  AND severity IN (:severity_one, :severity_two)
ORDER BY created_at DESC
LIMIT :row_limit;
```

Summarize event counts by severity:

```sql
SELECT severity, COUNT(*) AS event_count
FROM lab_events
WHERE created_at >= :start_time
  AND created_at < :end_time
GROUP BY severity
ORDER BY event_count DESC;
```

> Bind values with the database driver's parameterized-query API. Placeholder syntax varies by driver; never construct SQL by concatenating untrusted input.

## Security notes

- Use a read-only, least-privilege account for analysis where possible.
- Avoid `SELECT *` when only a subset of columns is needed.
- Validate and bind user-supplied values; allowlist identifiers that cannot be bound.
- Apply row limits and time bounds to reduce accidental over-collection.
- Do not log credentials or query results containing sensitive values.

## Results

- **Expected:** [Expected rows/aggregates]
- **Observed:** [Synthetic result]
- **Validation:** [How results were checked]

```text
[Paste synthetic, non-sensitive output]
```

## Screenshots

![Sanitized SQL lab result](../../assets/screenshots/REPLACE-WITH-SANITIZED-IMAGE.png)

## Lessons learned

[Explain query plan, edge cases, access controls, and limitations.]
