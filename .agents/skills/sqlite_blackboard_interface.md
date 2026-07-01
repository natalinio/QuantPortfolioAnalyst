# Skill: SQLite Blackboard Interface

Allows QPA agents to read and write states from the shared SQLite database.

## Details
- Connection String: `sqlite://data/qpa_blackboard.db`
- Supported operations:
  - SELECT queries across all 15 blackboard tables.
  - INSERT / UPDATE queries to write recommendations, risk constraints, opportunities, and logs.
