# Evaluation Rubric: Advanced Financial Modeling & Excel Analytics

## Overview
This rubric provides standard evaluation criteria for scoring LLM outputs on complex Excel tasks (e.g., dynamic financial statements, DCF models, LBO schedules, KPI dashboards, and VBA/LAMBDA functions).

---

## 1. Scoring Dimensions (Weighted 1–5 Scale)

| Metric ID | Dimension | Weight | Description |
| :--- | :--- | :--- | :--- |
| **M1** | **Formula Syntax & Dynamic Arrays** | 30% | Correctness of formulas (`XLOOKUP`, `INDEX/MATCH`, `LET`, `LAMBDA`, `OFFSET`). Avoids deprecated functions and hardcoded calculations. |
| **M2** | **Financial & Accounting Logic** | 25% | Accurate financial mechanics (Balance Sheet balancing, working capital changes, circular reference handling for interest/debt sweeps). |
| **M3** | **Instruction Adherence & Constraints** | 20% | Strict adherence to cell coordinates, requested sheet layouts, named ranges, and formatting parameters. |
| **M4** | **Financial Model Hygiene & UX** | 15% | Color coding standards (Blue = inputs, Black = formulas, Green = cross-sheet links), gridline settings, number formatting (`$#,##0;($#,##0);"-"`). |
| **M5** | **Edge-Case & Error Robustness** | 10% | Handling of division by zero (`IFERROR`, `DIV/0!`), leap years, non-operating items, and rate floor/cap edge cases. |

---

## 2. Rating Scale Definitions

### Score 5 (Mastery / Production-Ready)
* Formulas are modern, dynamic, and non-volatile.
* Zero hardcoded logic in calculations; dynamic scenario switches work seamlessly.
* Explicit cell-locking (`$A$1`) applied correctly across copy-paste directions.
* Follows FAST (Flexible, Appropriate, Structured, Transparent) financial modeling standards.

### Score 3 (Marginally Acceptable / Requires Human Revision)
* Model logic is mathematically correct but relies on inefficient legacy formulas (e.g., deeply nested `IF` statements instead of `SWITCH` or `IFS`).
* Minor cell reference locking errors that break when formulas are dragged horizontally.
* Number formatting is inconsistent or missing unit labels (e.g., ($M vs $K)).

### Score 1 (Failed / Hallucinated / Broken)
* Generates non-existent Excel functions or syntactically invalid formulas (e.g., unbalanced parentheses).
* Balance Sheet does not balance; cash flow statement ignores non-cash adjustments.
* Introduces unintended circular references.
