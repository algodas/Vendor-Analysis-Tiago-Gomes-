# Vendor Spend Due Diligence — Tiago Gomes (VP Ops / M&A)

## Overview
This repository contains a vendor spend due diligence analysis for an acquired company scenario. The goal was to:
- Categorize vendors by department
- Produce a concise, accurate one-line description per vendor
- Recommend an action per vendor (**Terminate / Consolidate / Optimize**)
- Identify the **Top 3 cost-saving opportunities**
- Document the methodology, prompts, and quality-control steps
- Provide a **CEO/CFO-ready executive memo** summarizing findings and next actions

The work is structured for fast executive review (CEO/CFO) while preserving traceability to the underlying vendor-level decisions.

---

## Links
**Claude Project (full working context, inputs/outputs, iterations):**  
https://claude.ai/project/019b7f8c-c569-771c-8d9d-c81141097e7e

**GitHub Repository:**  
https://github.com/algodas/Vendor-Analysis-Tiago-Gomes-/

---

## Repository Structure (Where to Find Everything)

### `/data/`
Contains:
- **Source vendor spend dataset** (as provided in the assessment)
- **Treated/cleaned datasets** after processing and quality checks (name normalization, dedupes, formatting)

If you want to compare “before vs. after” and review the inputs that drive the final decisions, start here.

### `/result/`
Contains the final deliverables, including the completed workbook with:
- **Part 1:** Vendor Analysis (Department / Description / Action per vendor)
- **Part 2:** Top 3 Opportunities (largest, most defensible savings levers)
- **Part 3:** Methodology (tools, prompts, validation steps)
- **Part 4:** CEO/CFO Executive Memo (1-page summary + 30/60/90-day plan)

For reviewers who want outcomes quickly, this is the primary folder.

---

## How to Review (Executive Path — ~3 Minutes)

1) Open `/result/` and download the final workbook  
2) Review tabs in this order:
   1. **Top 3 Opportunities** → fastest view of savings levers and assumptions  
   2. **CEOCFO Recommendations** → 1-page memo suitable for CEO/CFO consumption  
   3. **Vendor Analysis Assessment** → vendor-level classifications and actions (traceability)  
   4. **Methodology** → how it was done (tools, prompts, QC)

---

## Deliverables (What Was Produced)

### Part 1 — Vendor-Level Classification
For each vendor, the workbook includes:
- **Department** using a consistent taxonomy: **G&A, Sales, Finance, Engineering, Infrastructure, Marketing, Support**
- **One-line description** (CEO-friendly: “what it is / why we pay”)
- **Strategic recommendation** (exactly one per vendor):
  - **Terminate** → no longer needed / low ROI / redundant
  - **Consolidate** → overlap across vendors or fragmented footprint (multiple vendors doing the same job)
  - **Optimize** → strategically useful vendor, but spend can be reduced (licenses, usage, contract terms)

### Part 2 — Top 3 Strategic Opportunities (Highest-Impact Savings)
The analysis surfaces three executive-ready cost levers:
1. **Salesforce CRM footprint & license optimization**
2. **Real estate / co-working consolidation**
3. **Advisory & consulting rationalization**

Each opportunity includes:
- A summary title
- A brief explanation (2–4 sentences, CEO/CFO tone)
- A conservative annual savings estimate (USD) with clear assumptions

### Part 3 — Methodology
Documents:
- How the analysis was approached (taxonomy, vendor-level outputs, decision rules)
- Tools used
- Prompt patterns used to generate consistent results
- Validation and quality-control checks

### Part 4 — CEO/CFO Memo
A one-page memo that:
- Summarizes key findings
- Quantifies annualized savings range (conservative)
- Proposes a 30/60/90-day execution plan
- Introduces governance to prevent spend regrowth

---

## Interpretation Notes (How to Read the Output)
- **Consolidate** indicates duplication (multiple vendors serving the same function) or geographic fragmentation (many providers across regions).
- **Optimize** is applied to “must-have” vendors where spend is often reducible without impacting outcomes (e.g., license right-sizing, contract renegotiation, usage enforcement).
- **Terminate** is used conservatively and reserved for clearly redundant/low-value tools or services.
- Savings estimates are framed for CFO credibility; higher savings may be achievable after contract-level validation.

---

## AI + Quality Control (What Was Checked)
To ensure outputs are realistic, consistent, and reviewable:
- **Spend sanity checks:** top vendors map to expected departments (CRM, cloud, real estate, advisory)
- **Consistency sampling:** spot checks across vendors with similar functions (insurance, recruiting, office space, advisory)
- **Duplicate detection:** near-duplicate vendor names flagged for consolidation
- **Executive plausibility review:** avoided unrealistic reductions in core infrastructure; focused on fragmentation and underutilization

Full iterative context (inputs, prompts, refinements) is available via the Claude project link above.

---

## How to Reproduce / Extend (Reviewer-Friendly)
To extend this analysis:
1) Start from `/data/` (source + treated datasets)
2) Apply the same taxonomy and action rules documented in the **Methodology** tab
3) Re-run QC checks:
   - duplicates / name variants
   - category consistency
   - top-spend review by department
4) Update `/result/` deliverables:
   - vendor-level classifications
   - Top 3 Opportunities (recompute savings if assumptions change)
   - CEO/CFO memo (reflect any updated savings numbers or decisions)

---

## Ownership
**Tiago Gomes**  
Role simulation: **VP of Operations (AcquiredCo) — M&A Vendor Due Diligence**
