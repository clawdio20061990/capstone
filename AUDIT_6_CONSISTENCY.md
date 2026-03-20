# Audit 6: Cross-Document Numerical Consistency

**Date:** March 2026  
**Status:** RESOLVED — All critical and high-priority issues fixed  
**Scope:** FINANCIAL_ANALYSIS, LEAN_CANVAS, HARDWARE_COST_OPERATIONAL_BUDGET, PITCH_DECK_STRUCTURE, PITCH_DECK_5MIN, BUSINESS_RESEARCH, SWOT_ANALYSIS, MASTER_DATA_SHEET

---

## Canonical Numbers (Source of Truth)

All documents now use these consistent figures:

| Metric | Value | Calculation |
|--------|-------|-------------|
| Retail Price | €150 | DTC only |
| Y1 COGS (midpoint) | €99.50 | Range €95–104, midpoint used |
| Y2 COGS (blended) | €90 | 70% RPi €99.50 + 30% custom PCB €68 |
| Y3 COGS (custom PCB) | €75 | Full custom PCB at scale |
| Fulfillment Y1–2 | €9/unit | DTC shipping + packaging |
| Fulfillment Y3 | €8.50/unit | Regional distribution centers |
| **Hardware Margin Y1** | **€41.50** | €150 – €99.50 – €9 |
| **Hardware Margin Y2** | **€51** | €150 – €90 – €9 |
| **Hardware Margin Y3** | **€66.50** | €150 – €75 – €8.50 |
| EU+UK Cats | 127M+ | FEDIAF 2024 |
| Annual Retention | 70% | Industry upper quartile |
| Monthly Churn | ~2.9% | 1 – 0.70^(1/12) ≈ 2.9% |
| Trial Signup | 25% of buyers | |
| Trial-to-Paid | 50% of trial users | |
| **Effective Conversion** | **12.5%** | 25% × 50% |
| ARPU Y1–2 | €4.50/month | Std €3 × 50% + Premium €6 × 50% |
| ARPU Y3+ | €4.90/month | Std €3 × 50% + Prem €6 × 30% + Ultra €8 × 20% |
| LTV per Subscriber | €200 | €41.50 hw + €158 sub (5-year, 70% retention) |
| LTV per Buyer | €61 | €41.50 hw + 12.5% × €158 sub |

---

## Issue Status

### CRITICAL — All Fixed

#### 1. COGS vs Margins ✅ FIXED
**Problem:** Year 1 margin stated as €42, but €150 – COGS – fulfillment didn't add up with varying COGS figures (€95, €104, €99.50).  
**Fix:** Unified Y1 COGS to €99.50 (midpoint). Margin = €150 – €99.50 – €9 = **€41.50**. Applied consistently in FINANCIAL_ANALYSIS (Sections 1.1, 2.1, 3.1, 6.1), LEAN_CANVAS (Unit Economics, Revenue Streams, Cost Structure), HARDWARE_COST_OPERATIONAL_BUDGET (Reconciliation, COGS Summary), BUSINESS_RESEARCH (Unit Economics), MASTER_DATA_SHEET.

#### 2. Gross Margin % ✅ FIXED
**Problem:** Gross margin percentages didn't account for subscription revenue in denominator or were inconsistent.  
**Fix:** Recalculated properly: Y1 24.6%, Y2 31.9%, Y3 42.7%. Formula: (Total Revenue – Total COGS) / Total Revenue. Total COGS includes hardware BOM, fulfillment, payment processing, and customer support. Updated in FINANCIAL_ANALYSIS and LEAN_CANVAS.

#### 3. "50M cats" vs "127M cats" ✅ FIXED
**Problem:** Pitch decks said "50M+ cats" while SWOT and BUSINESS_RESEARCH correctly used FEDIAF figure of 127M.  
**Fix:** Updated PITCH_DECK_STRUCTURE (Slides 1, 2, speaker notes) and PITCH_DECK_5MIN (Slide 2, speaker notes) to "127M+ cats in EU + UK." Updated MASTER_DATA_SHEET.

### HIGH — All Fixed

#### 4. Retention 70% vs Churn <4%/<5% ✅ FIXED
**Problem:** 70% annual retention = 30% annual churn = ~2.9% monthly churn. Documents variously stated "<4%" or "<5%".  
**Fix:** All references in scope documents now state "~2.9% monthly churn" or "<3% monthly churn" consistently. Updated: FINANCIAL_ANALYSIS (LTV methodology, Series A metrics), LEAN_CANVAS (Product Metrics, Series A Triggers), PITCH_DECK_STRUCTURE, PITCH_DECK_5MIN, BUSINESS_RESEARCH.  
**Note:** TECHNOLOGY_PRODUCT_ROADMAP (Section 6) and MARKETING_STRATEGY (Section 8) have tiered churn targets (<5%/<4%/<3%) that represent aspirational milestones — these are outside current fix scope but should be reviewed for consistency.

#### 5. Subscription Revenue Ramp ✅ FIXED
**Problem:** Y1 subscription revenue of €8,100 assumed 150 subscribers for all 12 months. In reality, subscribers ramp from 0 during Months 7–12.  
**Fix:** Recalculated with proper ramp:
- Y1: €4,050 (~75 avg subs × €4.50 × 12; end-of-year run-rate €675/month)
- Y2: €27,594 (carryover €5,670 + new ~€21,924)
- Y3: €103,899 (carryover Y1 €4,292 + carryover Y2 €33,457 + new €66,150)
- Total Revenue: Y1 €184K, Y2 €1.003M, Y3 €2.80M
- Net Income: Y1 -€339K, Y2 -€332K, Y3 +€213K

Updated in FINANCIAL_ANALYSIS (Sections 2.1–2.3, Summary Table), LEAN_CANVAS (Revenue Streams, Growth Metrics), HARDWARE_COST_OPERATIONAL_BUDGET (Reconciliation).

#### 6. LTV per Buyer €62 → €61 ✅ FIXED
**Problem:** Calculation not shown; didn't reconcile with stated inputs.  
**Fix:** Explicit calculation now in FINANCIAL_ANALYSIS Section 1.2:
- LTV per buyer = €41.50 hardware margin + (12.5% effective conversion × €158 subscription LTV) = €41.50 + €19.78 = **€61**
- Updated in all documents: FINANCIAL_ANALYSIS, LEAN_CANVAS, BUSINESS_RESEARCH.

#### 7. LTV per Subscriber €200 ✅ FIXED
**Problem:** Calculation not fully transparent.  
**Fix:** Explicit year-by-year calculation now in FINANCIAL_ANALYSIS Section 1.2:
- Y1: €4.50 × 12 = €54.00
- Y2: €4.90 × 12 × 0.70 = €41.16
- Y3: €4.90 × 12 × 0.70² = €28.81
- Y4: €4.90 × 12 × 0.70³ = €20.17
- Y5: €4.90 × 12 × 0.70⁴ = €14.12
- Total subscription: €158.26 ≈ €158
- Total LTV: €41.50 + €158 = **€199.50 ≈ €200** ✓

#### 8. "50% Conversion" Clarity ✅ FIXED
**Problem:** "50% conversion" was ambiguous — could mean 50% of buyers or 50% of trial users.  
**Fix:** All documents now clearly state the two-step funnel:
- 25% of hardware buyers sign up for free trial
- 50% of trial users convert to paid ("trial-to-paid conversion")
- **12.5% effective conversion** of all hardware buyers to paying subscribers
- Terminology "trial-to-paid" used consistently; "effective conversion" defined wherever the funnel is mentioned.

---

## Out-of-Scope Items (Not Fixed in This Pass)

The following files contain numbers that should also be updated but were outside the assigned scope:

| File | Issue | Status |
|------|-------|--------|
| MARKETING_STRATEGY.md | References €42 margin, €62 LTV, €8.1K subscription | NEEDS UPDATE |
| TECHNOLOGY_PRODUCT_ROADMAP.md | Churn targets <5%/<4%/<3% (aspirational tiers) | REVIEW NEEDED |
| RISK_ANALYSIS.md | May reference old subscription/LTV figures | NEEDS REVIEW |
| PRODUCT_CONCEPT.md | References "30% gross margin" Y1 | NEEDS UPDATE |
| OPERATIONS.md | May reference old COGS figures | NEEDS REVIEW |

---

## Summary

All 8 identified issues (3 Critical, 5 High) have been resolved in the 7 assigned source files plus MASTER_DATA_SHEET. Numbers are now internally consistent and mathematically verifiable. The slightly optimistic MBA capstone tone is preserved while ensuring all figures are defensible under scrutiny.

**Key cascading changes from fixes:**
- Total Y3 revenue: €2.85M → €2.80M (due to subscription ramp correction)
- Y3 Net Income: +€253K → +€213K
- Cumulative break-even: Month 32–33 → Month 33–34
- All changes are directionally conservative, strengthening credibility of the model.
