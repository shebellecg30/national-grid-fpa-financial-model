# Automated Model Integrity Checks

The Excel model includes a dedicated `15_CHECKS` worksheet with 16 automated integrity checks.

At the current model state, all checks return **PASS**.

| ID | Model Area | Check |
|---|---|---|
| CHK-01 | Balance Sheet | Total Assets = Total Liabilities & Equity |
| CHK-02 | Cash Flow | Opening Cash + Net Change + FX = Ending Cash |
| CHK-03 | 3-Statement Link | Cash Flow ending cash = Balance Sheet cash |
| CHK-04 | PP&E Schedule | PP&E roll-forward |
| CHK-05 | PP&E / Balance Sheet | PP&E schedule = Balance Sheet PP&E |
| CHK-06 | Debt Schedule | Debt roll-forward |
| CHK-07 | Debt / Balance Sheet | Debt schedule = Balance Sheet borrowings |
| CHK-08 | Debt / Income Statement | Finance cost tie-out |
| CHK-09 | Income Statement | PBT + Tax = PAT |
| CHK-10 | Income Statement | Revenue × Operating Margin = Operating Profit |
| CHK-11 | Equity | Equity roll-forward |
| CHK-12 | Scenarios | Base scenario = FY2027 core forecast |
| CHK-13 | DCF | Enterprise Value bridge |
| CHK-14 | DCF | Enterprise Value to Equity Value bridge |
| CHK-15 | DCF | Implied share price calculation |
| CHK-16 | Liquidity | Forecast ending cash = minimum cash assumption |

A tolerance of £0.1m is used where relevant to prevent immaterial floating-point differences from generating false failures.
