# Shared Decision Taxonomy

All QPA agents must use the following controlled action vocabulary when recommending portfolio transactions:

| Action | Meaning |
|---|---|
| `OPEN` | Open a new position not currently held. |
| `INCREASE` | Increase an existing position. |
| `REDUCE` | Reduce an existing position. |
| `CLOSE` | Fully close an existing position. |
| `HOLD` | Maintain the position with no action. |
| `WAIT` | Valid action deferred due to timing, risk or execution constraints. |
| `REVIEW_REQUIRED` | Human validation required due to missing data, conflict or uncertainty. |

## Execution Status Categories
When recommendations are finalized, they must receive one of the following execution statuses:
- `APPROVED`: Reconciled and passed risk constraint checks.
- `VETOED`: Blocked by a hard risk concentration or turnover constraint.
- `DEFERRED`: Deferred due to timing or softer trading limits.
- `REVIEW_REQUIRED`: Requires manual compliance review.
- `DATA_QUALITY_BLOCKED`: Critical or high data quality issue blocks transaction.
