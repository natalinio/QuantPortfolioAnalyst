# Skill: Recommendation Writer

Enables agents to write their recommendations and structured explanations directly onto the SQLite blackboard.

## Details
- Interface: Parameterized SQL inserts.
- Updates table: `agent_recommendations`, `final_recommendations`.
- Enforces: Pydantic schema validation before writing.
