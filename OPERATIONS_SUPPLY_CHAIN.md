# Operations & Supply Chain Plan

**Document Version:** 1.0  
**Date:** March 2026  
**Scope:** High-level operational framework for manufacturing, fulfillment, quality, and customer support  
**Integration:** Complements Financial Analysis, Hardware Cost Analysis, and Risk Analysis

---

## 1. Supply Chain Overview

### 1.1 Sourcing Strategy

Reactacat operates a **hybrid sourcing model**: electronic components sourced globally (authorized distributors), with assembly and enclosure manufacturing localized in Poland/EU.

**Tier 1 Suppliers (critical components):**
- **Processing unit:** Raspberry Pi 4B via authorized EU distributors (Year 1); custom PCB via European EMS partner (Year 2+)
- **Camera module:** OV5647 from Arducam or equivalent, dual-sourced
- **Servo motors:** MG90S from TowerPro (primary) + alternative supplier (backup)
- **Laser module:** EU-compliant 650nm diode from certified supplier

**Tier 2 Suppliers (enclosure, packaging):**
- **Injection molding:** Polish contract manufacturer for enclosure production
- **Packaging:** Polish packaging supplier for retail boxes and inserts

**Principle:** No single-source dependency for any critical component. Minimum two qualified suppliers per component category by end of Year 1.

### 1.2 Inventory Policy

| Phase | Strategy | Buffer Stock | Rationale |
|-------|----------|-------------|-----------|
| **Year 1 (1,200 units)** | Build-to-stock, small batches | 2–3 months | Mitigate RPi supply risk; learn demand patterns |
| **Year 2 (6,500 units)** | Build-to-forecast | 1–2 months | Stabilized demand signal; multi-market logistics |
| **Year 3 (18,000 units)** | Build-to-demand | 1 month | Mature forecasting; regional distribution |

Reorder point: when inventory drops below 6-week sales forecast. Safety stock maintained for seasonal spikes (Q4 holiday demand).

---

## 2. Manufacturing Operations

### 2.1 Assembly Model

**Year 1–2:** Outsourced to European contract manufacturer (CM) in Poland.  
**Year 3+:** Evaluate in-house assembly if volume exceeds 20,000 units/year.

The CM handles: component receiving, PCB/RPi mounting, servo and laser integration, wiring, firmware flashing, functional testing, packaging, and labeling.

Reactacat retains: product design, BOM management, firmware development, quality specifications, and final acceptance criteria.

### 2.2 Production Workflow

```
Component Procurement (4–6 weeks lead)
        ↓
Incoming Inspection (CM)
        ↓
Assembly (25 min/unit)
        ↓
Firmware Flash + Device Provisioning
        ↓
Functional Test + Laser Safety Check
        ↓
Packaging + Labeling
        ↓
Finished Goods Warehouse
        ↓
Fulfillment (ship to customer)
```

### 2.3 Production Batches

| Year | Batch Size | Frequency | Annual Output |
|------|-----------|-----------|---------------|
| 1 | 200–300 units | Every 6–8 weeks | 1,200 |
| 2 | 500–800 units | Monthly | 6,500 |
| 3 | 1,500–2,000 units | Bi-weekly | 18,000 |

Small, frequent batches reduce inventory risk and allow rapid incorporation of design improvements.

---

## 3. Quality Assurance

### 3.1 Quality Framework

Three-gate inspection process:

1. **Incoming:** Verify component specifications against BOM. Sample testing (AQL 2.5 for electronics, AQL 4.0 for mechanical parts)
2. **In-process:** Servo alignment check + laser output verification at mid-assembly
3. **Final:** Full functional test — WiFi connectivity, camera feed, servo range of motion, laser output power, treat dispenser operation (if included), firmware boot verification

### 3.2 Acceptance Criteria

- Hardware defect target: <3% (Year 1), <2% (Year 2), <1.5% (Year 3)
- Customer return target: <5% (Year 1), <3% (Year 2)
- Mean Time Between Failures (MTBF): >5,000 operating hours

Failed units are repaired or recycled. Root cause analysis for any defect occurring in >1% of units.

---

## 4. Fulfillment & Logistics

### 4.1 Distribution Model

**Year 1 (Poland):** Direct-to-consumer, shipped from CM warehouse or small 3PL in Warsaw. Standard courier delivery (DPD, InPost, Poczta Polska). Target: 2–3 day delivery within Poland.

**Year 2 (EU expansion):** Regional 3PL partners in Germany and UK for local fulfillment. Cross-border shipping from Poland for France (until volume justifies local 3PL). Target: 3–5 day delivery within EU.

**Year 3 (scaled):** Multi-node fulfillment network across 3–4 EU locations. Amazon FBA considered as supplementary channel (adds ~15% fee but provides Prime delivery and marketplace visibility).

### 4.2 Fulfillment Costs

| Component | Year 1 | Year 2 | Year 3 |
|-----------|--------|--------|--------|
| **Picking/packing** | €2.00 | €1.80 | €1.50 |
| **Shipping (avg)** | €5.50 | €5.50 | €5.00 |
| **Returns processing** | €1.50 (allocated) | €1.20 | €1.00 |
| **Total per unit** | **€9.00** | **€8.50** | **€7.50** |

Consistent with Financial Analysis fulfillment assumption (€9 Year 1, €8.50 Year 3).

### 4.3 Returns & Reverse Logistics

- **Return window:** 30 days no-questions-asked (exceeds EU 14-day minimum — builds trust)
- **Process:** Customer initiates return via app/website → prepaid label generated → unit returned to CM → inspection → refurbish or recycle
- **Refurbishment:** Functional returned units cleaned, re-tested, and sold as "Certified Refurbished" at 15–20% discount (Year 2+)

---

## 5. Customer Support

### 5.1 Support Model

| Channel | Availability | Year 1 | Year 2+ |
|---------|-------------|--------|---------|
| **Email** | Business hours (9–18 CET) | In-house (founder team) | Outsourced + in-house escalation |
| **In-app chat** | Business hours | Chatbot + human fallback | Chatbot + outsourced agents |
| **Knowledge base** | 24/7 | Self-service articles, FAQs, video tutorials | Expanded, localized |
| **Phone** | Not offered initially | — | Evaluate based on demand |

### 5.2 Support Costs

Budgeted at €0.50 per active customer per month (Financial Analysis). At 450 active customers (Year 1 average), this is €2,700/year — covered within operational budget.

### 5.3 Support KPIs

- First response time: <4 hours (business hours)
- Resolution time: <24 hours for standard issues, <72 hours for hardware replacements
- Customer satisfaction (CSAT): >85%
- Support ticket rate: <10% of active customers per month

---

## 6. Technology Operations

### 6.1 Cloud Infrastructure

AWS-based backend (SageMaker for ML, IoT Core for device management, S3 for data, RDS for user database). See Hardware Cost Analysis, Section 4 for detailed per-device cost model.

**Key operational requirements:**
- **Uptime SLA:** 99.5% for API and device management services
- **OTA updates:** Firmware pushed to devices via AWS IoT Core. Staged rollout (10% → 50% → 100%) to catch issues early
- **Monitoring:** CloudWatch alerts for API errors, device connectivity drops, and ML pipeline failures
- **Backup:** Daily automated database backups. 30-day retention. Disaster recovery plan documented

### 6.2 Device Lifecycle Management

```
Manufacturing → Provisioning → Active Use → Subscription → End of Life
```

Each device receives a unique identity at provisioning (device certificate). Cloud tracks: firmware version, last connection, gameplay sessions, subscription status, warranty expiry.

**End of Life (EOL):** WEEE-compliant recycling program. Free return shipping for EOL devices. Recycled through registered EU waste electronics processor.

---

## 7. Scaling Considerations

### 7.1 Operational Milestones

| Milestone | Trigger | Action |
|-----------|---------|--------|
| **1,000 units cumulative** | Month 10–12 | Formalize CM relationship; negotiate volume pricing |
| **5,000 units cumulative** | Month 18–20 | Transition to custom PCB; add regional 3PL |
| **10,000 units cumulative** | Month 24–28 | Multi-cavity mold upgrade; evaluate Amazon FBA |
| **25,000 units cumulative** | Year 3+ | Evaluate in-house assembly; hire ops manager |

### 7.2 Team Scaling

| Role | Year 1 | Year 2 | Year 3 |
|------|--------|--------|--------|
| CTO / Co-founder | 1 | 1 | 1 |
| Software Engineer | 1 | 1 | 2 |
| Marketing / Ops Manager | — | 1 | 1 |
| **Total FTE** | **2** | **3** | **4** |

Customer support, accounting, legal, and logistics outsourced until volume justifies in-house roles.

---

## References

- Financial Analysis Document. (2026, March). *Financial Analysis: Reactacat 3-Year Projection & Funding Model.*
- Hardware Cost Analysis & Operational Budget Document. (2026, March). *Hardware Cost Analysis & Operational Budget.*
- Risk Analysis Document. (2026, March). *Risk Analysis: Comprehensive Risk Assessment & Mitigation Plan.*
- Marketing Strategy Document. (2026, March). *Marketing Strategy: Reactacat Go-to-Market & Growth Plan.*

---

**Document Status: COMPLETE**  
**Scope Note:** This document provides a strategic operational framework. Detailed process documentation, supplier contracts, and SOP manuals will be developed during Months 1–6 as part of pre-launch preparation.
