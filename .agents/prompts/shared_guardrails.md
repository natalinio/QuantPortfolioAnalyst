# Shared Guardrails

1. **No Hallucinated Data**: Never invent pricing, yields, indicators, or look-through details. If data is absent, flag it.
2. **Deterministic Computation Separation**: Do not calculate financial metrics (YTM, duration, returns, weights) inside LLM prompts. Always read them from the database.
3. **Auditability**: Every recommendation must be accompanied by structured quantitative evidence referencing actual values stored in the database.
4. **Veto Overrides**: Original gross recommendations must never be modified. If overridden or vetoed, preserve the gross recommendation and explain the override in detail.
