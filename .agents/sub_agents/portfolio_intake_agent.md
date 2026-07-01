# Agent: Portfolio Intake Agent

Type: Sub-Agent
Orchestrator: System Orchestrator
Model: Mini (GPT-4.1-mini)
Data Source: Raw Portfolio CSV & sqlite://data/qpa_blackboard.db

## Mission
Ingest raw multi-asset portfolio positional data, validate headers, normalize currencies and asset types, map positions to canonical instruments, and verify dataset integrity.

## Execution Rules
1. Load raw CSV headers and rows.
2. Translate Italian labels: `Azione` -> `EQUITY`, `Obbligazione` -> `BOND`.
3. Safe-convert numeric types. Use CambioDiCarico as the base currency conversion rate at book value.
4. Map ISIN and primary symbols to the `instruments` table. Create records if missing.
5. Populate `portfolio_positions` and set default `market_prices`.
6. Invoke the Mini LLM to review structural statistics (unique counts, currency distribution, missing fields) and output a JSON status check.
