# 📊 Enterprise Document AI Evaluation Suite & Benchmark (Excel, PowerPoint, Word)

An industry-grade evaluation framework designed to benchmark, evaluate, and fine-tune Large Language Models (LLMs) and AI agents on Fortune 500-level business deliverables.

## 🎯 Purpose
AI models frequently fail on nuance, complex syntax (e.g., nested dynamic arrays in Excel), executive synthesis (Word), and visual hierarchy/slide logic (PowerPoint). This repository provides:
1. **Realistic Enterprise Prompt Scenarios**: Multi-turn, instruction-dense prompts modeled after Tier-1 investment banking, management consulting, and corporate strategy tasks.
2. **Structured AI Evaluation Rubrics**: Domain-specific grading frameworks across Accuracy, Format Compliance, Executive Tone, and Hallucination Index.
3. **Model Benchmark & Side-by-Side Analysis**: Real evaluation logs comparing frontier models (GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Pro) on complex office deliverables.

---

## 🛠️ Taxonomy & Evaluation Dimensions

All models are evaluated on a 1–5 Likert scale across 5 core dimensions:

| Metric | Description | Weight |
| :--- | :--- | :--- |
| **Domain Accuracy & Logic** | Precision of financial formulas, accounting logic, data integrity, and factual consistency. | 30% |
| **Instruction Adherence** | Strict adherence to constraints (e.g., cell reference locks, word counts, formatting tokens). | 25% |
| **Executive Synthesis** | C-suite clarity, MECE structure, bottom-line-up-front (BLUF) formatting. | 20% |
| **Format & Schema Execution** | Valid VBA/Python script generation, XML syntax, Excel formula nestings, slide deck layouts. | 15% |
| **Hallucination & Error Rate** | Presence of non-existent Excel functions, circular logic, or unverified financial claims. | 10% |

---

## 📁 Repository Highlights

### 1. Advanced Excel Benchmark: 3-Statement & DCF Modeling
* **Scenario**: Prompting models to build a dynamic 5-year DCF model with WACC calculation, scenario toggles (`INDEX/MATCH`, `XLOOKUP`), and sensitivity tables (`DATA TABLE`).
* **Evaluation Focus**: Formula syntax verification, circular reference prevention, dynamic range accuracy, and macro/VBA automation integrity.
* 📄 [View Excel Evaluation Log](evaluations/excel-dcf-model-comparison.md)

### 2. PowerPoint Benchmark: Board-Level QBR & Strategy Decks
* **Scenario**: Transforming unstructured operational KPI data into a structured 5-slide Executive Pitch Deck following Pyramid Principle formatting.
* **Evaluation Focus**: Cognitive load distribution, actionable slide titles (action-oriented leads), narrative flow, and table/chart visual layout recommendations.
* 📄 [View PowerPoint Evaluation Log](evaluations/ppt-strategy-deck-critique.md)

### 3. Word Benchmark: M&A Strategic Due Diligence Memo
* **Scenario**: Drafting a 3-page C-Suite Investment Committee briefing covering risk factors, synergy quantification, and valuation summaries.
* **Evaluation Focus**: Tone calibration (balanced/objective), structured header hierarchy, and concise executive summary formatting.
* 📄 [View Word Evaluation Log](evaluations/word-board-memo-assessment.md)

---

## 🔬 Sample Prompt & Evaluation Architecture

### Scenario ID: `FIN-XL-004` (Dynamic LBO Debt Schedule)
```json
{
  "scenario_id": "FIN-XL-004",
  "domain": "Corporate Finance / Private Equity",
  "complexity": "Tier-3 Advanced",
  "prompt": "Construct a dynamic debt amortization schedule in Excel for a $500M senior secured credit facility with a 5-year tenor, SOFR + 325 bps interest margin, 1% SOFR floor, 10% annual mandatory amortization, and a 50% excess cash flow sweep mechanism. Provide cell-specific formulas using modern dynamic array functions (LAMBDA / LET where appropriate)."
}
