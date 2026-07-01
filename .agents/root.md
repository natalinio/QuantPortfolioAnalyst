# Antigravity ADK Root Agent Configuration

System Name: Multi-Agent Quantamental Portfolio Analyst (QPA)
Orchestration Pattern: SQLite Blackboard Pattern
Blackboard Database: sqlite://data/qpa_blackboard.db

## System Objective
To ingest raw multi-asset and multi-currency portfolio position records, run data quality validations, run specialized asset analysts, evaluate aggregate risk, seek alpha opportunities to cover exposure gaps, and reconcile all advice into a final, explainable recommendation matrix.

## Agent Architecture
The system consists of the following agents:
1. **Portfolio Intake Agent** (Mini Model) - Handles data loading and verification.
2. **Macro Market Sentinel Agent** (Mini Model) - Ingests general business/geopolitical news and sets the global macro regime/bias.
3. **Equity Analyst Agent** (Pro Model) - Evaluates valuation and technical momentum of equities.
4. **Bond Analyst Agent** (Pro Model) - Evaluates fixed-income duration, yields, and seniority.
5. **ETF / ETC Analyst Agent** (Mini Model) - Decomposes fund constituents and checks overlapping exposure.
6. **Risk & Macro Rebalancing Agent** (Pro Model) - Computes exposures and evaluates concentration limits.
7. **Alpha Generator Agent** (Mini Model) - Proposes external buys to address low weight exposure gaps.
8. **CIO Supervisor Agent** (Pro Model) - Resolves conflicts, applies vetoes, and generates final reports.
