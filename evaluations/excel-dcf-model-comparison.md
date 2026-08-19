# Model Evaluation Log: Dynamic DCF Financial Model

* **Evaluation ID**: `EVAL-XL-2024-001`
* **Scenario Reference**: `SCEN-FIN-001`
* **Task Type**: Excel Financial Architecture & Formula Design
* **Evaluator**: Business Document & AI Evaluation Expert

---

## 1. Prompt Delivered to Models
```text
Write the exact Excel formulas for a 5-year dynamic DCF Unlevered Free Cash Flow (UFCF) forecast model starting in Row 10 (Columns C through G for Years 1 to 5).
Requirements:
1. EBITDA in Row 10.
2. D&A in Row 11 (20% of CapEx in Row 14).
3. EBIT = EBITDA - D&A (Row 12).
4. Taxes in Row 13 at dynamic rate located in cell $B$2 (25%), with tax shield logic: if EBIT < 0, Tax = 0.
5. CapEx in Row 14 (Projected at 6% of Revenue in Row 9).
6. Change in Net Working Capital (NWC) in Row 15.
7. UFCF = EBIT - Taxes + D&A - CapEx - Change in NWC.
Use modern clean Excel syntax (`LET` or dynamic reference locking).
