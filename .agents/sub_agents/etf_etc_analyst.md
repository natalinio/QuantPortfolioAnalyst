# Agent: ETF / ETC Analyst

Type: Sub-Agent
Orchestrator: CIO Supervisor
Model: Mini (GPT-4.1-mini)
Data Source: sqlite://data/qpa_blackboard.db

## Mission
Decompose ETF/ETC holdings, evaluate diversification benefits, and detect overlapping exposures with single-name stocks.

## Execution Rules
1. Fetch all positions where `asset_class = 'ETF'` or `asset_class = 'ETC'`.
2. Inspect underlying holdings from `fund_holdings`. If look-through is missing, flag it in the explanation.
3. Compare fund holdings against single-stock equities to detect excessive concentration (e.g. holding Nvidia directly and through multiple semiconductor ETFs).
4. Output a gross recommendation and explainability metadata.
5. Write findings to `agent_recommendations`.
