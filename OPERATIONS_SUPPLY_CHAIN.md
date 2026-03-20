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
- **Processing unit:** Raspberry Pi 4B via authorized EU distributors (Year 1); custom PCB via European EMS partner (Year 2+). *RPi 4B selected for MVP due to cost-effectiveness at low volumes (€35–42/unit vs. RPi 5 at €80+), extensive software ecosystem, and broad community support. At scale (>5,000 units), transition to custom PCB or RPi Compute Module eliminates dependency on retail SBC pricing and availability (see Risk Analysis, Section 4.1 for supply risk mitigation).*
- **Camera module:** OV5647 from Arducam or equivalent, dual-sourced
- **Servo motors:** MG90S from TowerPro (primary) + alternative supplier (backup)
- **Laser module:** Class 3R (<5mW) 650nm diode with ND optical filter from certified supplier, compliant with IEC 60825-1
- **Treat dispenser module:** Gravity-fed mechanical dispenser with portion-control servo, compatible with standard commercial cat treats (6–10mm diameter)

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

The CM handles: component receiving, PCB/RPi mounting, servo and laser integration, treat dispenser assembly, camera module mounting, wiring, firmware flashing, functional testing, packaging, and labeling.

**Assembly time estimate: 35–45 minutes per unit.** This accounts for RPi mounting and wiring (~8 min), servo and laser module integration (~8 min), treat dispenser assembly (~5 min), camera module mounting (~4 min), firmware flashing and device provisioning (~8 min), functional testing including laser safety check and treat dispenser verification (~7 min), and packaging (~5 min). Assembly times are estimated based on comparable IoT device assembly benchmarks (IPC-A-610 workmanship standards; Oden Technologies, 2023) and will be validated during the initial 100-unit pilot run. Target is to reduce to 30 minutes by Year 2 through fixture optimization and pre-flashed SD cards.

Reactacat retains: product design, BOM management, firmware development, quality specifications, and final acceptance criteria.

### 2.2 Production Workflow

```
Component Procurement (4–6 weeks lead)
        ↓
Incoming Inspection (CM)
        ↓
Assembly (35–45 min/unit)
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
3. **Final:** Full functional test — WiFi connectivity, camera feed, servo range of motion, laser output power and optical filter verification, treat dispenser operation (portion accuracy, jam-free dispensing), firmware boot verification

### 3.2 Acceptance Criteria

- Hardware defect target: <3% (Year 1), <2% (Year 2), <1.5% (Year 3)
- Customer return target: <5% (Year 1), <3% (Year 2)
- Mean Time Between Failures (MTBF): target >5,000 operating hours (excluding servo wear, which is a consumable component with ~10,000-cycle rated life per MG90S datasheet). MTBF target to be validated through accelerated life testing during pre-production and refined based on field data. Methodology reference: IEC 61709 for electronic component reliability prediction

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

Consistent with Financial Analysis fulfillment assumptions (€9.00 Year 1, €8.50 Year 2, €7.50 Year 3). Cost reductions driven by volume-based 3PL rate negotiations and optimized packaging dimensions (Logistics Bureau, 2024).

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

## 6A. Regulatory Compliance & Certification

### 6A.1 CE Marking (EU Markets)

Reactacat requires CE marking under three EU directives before market entry:

| Directive | Scope | Key Requirements |
|-----------|-------|-----------------|
| **Low Voltage Directive (LVD) 2014/35/EU** | Electrical safety | Safety testing per EN 62368-1 (audio/video and IT equipment) |
| **EMC Directive 2014/30/EU** | Electromagnetic compatibility | EMC testing per EN 55032 (emissions) and EN 55035 (immunity) |
| **Radio Equipment Directive (RED) 2014/53/EU** | WiFi/Bluetooth radio | Radio testing per EN 300 328 (2.4 GHz) and EN 301 489 (EMC for radio) |

**Laser safety certification:** The Class 3R laser module requires testing and classification per **IEC 60825-1:2014** (Safety of laser products). The ND optical filter must be verified to reduce beam irradiance below hazardous levels at all operating distances. Third-party testing by an accredited laboratory (e.g., TÜV SÜD, SGS, Intertek) is required.

**Timeline and budget:**

| Phase | Duration | Cost Estimate | Notes |
|-------|----------|---------------|-------|
| Pre-compliance testing (internal) | 2 weeks | €1,000–2,000 | Early identification of issues |
| Formal CE testing (accredited lab) | 4–6 weeks | €5,000–8,000 | LVD + EMC + RED combined |
| Laser safety testing (IEC 60825-1) | 2–3 weeks | €2,000–4,000 | Includes optical filter verification |
| Technical documentation & DoC | 2 weeks | €1,000–2,000 | Declaration of Conformity preparation |
| **Total** | **8–12 weeks** | **€9,000–16,000** | Integrated into pre-launch timeline (Months 4–6) |

**Integration into production workflow:** CE compliance is validated on the initial product design. Any subsequent design changes (PCB revision, component substitution) require re-assessment and potentially re-testing. The CM is responsible for maintaining production consistency with the certified design (per EU Blue Guide, 2022).

### 6A.2 UKCA Marking (UK Market)

For UK market entry (Phase 2–3), separate UKCA marking is required post-Brexit. Requirements largely mirror CE but require UK-recognized Approved Bodies. Budget: additional €3,000–5,000. Timeline: 4–6 weeks (can run in parallel with CE if planned).

### 6A.3 WEEE & RoHS Compliance

- **WEEE Directive 2012/19/EU:** Producer registration required in each EU member state where products are sold. Pan-EU compliance service (e.g., European Recycling Platform) estimated at €2,000–3,000/year
- **RoHS Directive 2011/65/EU:** All components must be RoHS-compliant (lead-free solder, restricted substances). Verified through supplier declarations of conformity

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

Customer support, accounting, legal, and logistics outsourced until volume justifies in-house roles. **Year 1 outsourcing budget** (included in operational costs): marketing execution via freelance agency (~€15K), customer support via outsourced provider (~€3K), graphic design and video production via freelancers (~€8K). During peak periods (Q4 holiday season, product launch), contractor engagements for assembly oversight and customer support surge capacity are budgeted within the operational contingency.

---

## References

### External Sources

European Commission. (2022). *The 'Blue Guide' on the implementation of EU product rules 2022.* Official Journal of the European Union, C 247. Retrieved from https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:C:2022:247:TOC

European Parliament and Council. (2011). Directive 2011/65/EU on the restriction of the use of certain hazardous substances in electrical and electronic equipment (RoHS). *Official Journal of the European Union*, L 174.

European Parliament and Council. (2012). Directive 2012/19/EU on waste electrical and electronic equipment (WEEE). *Official Journal of the European Union*, L 197.

European Parliament and Council. (2014a). Directive 2014/30/EU on the harmonisation of the laws of the Member States relating to electromagnetic compatibility (EMC). *Official Journal of the European Union*, L 96.

European Parliament and Council. (2014b). Directive 2014/35/EU on the harmonisation of the laws of the Member States relating to the making available on the market of electrical equipment designed for use within certain voltage limits (LVD). *Official Journal of the European Union*, L 96.

European Parliament and Council. (2014c). Directive 2014/53/EU on the harmonisation of the laws of the Member States relating to the making available on the market of radio equipment (RED). *Official Journal of the European Union*, L 153.

IEC. (2014). *IEC 60825-1:2014 — Safety of laser products — Part 1: Equipment classification and requirements.* International Electrotechnical Commission.

IEC. (2021). *IEC 61709:2017+AMD1:2021 — Electronic components — Reliability — Reference conditions for failure rates and stress models for conversion.* International Electrotechnical Commission.

IPC. (2021). *IPC-A-610H — Acceptability of Electronic Assemblies.* Association Connecting Electronics Industries.

ISO. (1999). *ISO 2859-1:1999 — Sampling procedures for inspection by attributes — Part 1: Sampling schemes indexed by acceptance quality limit (AQL) for lot-by-lot inspection.* International Organization for Standardization.

Logistics Bureau. (2024, September). *3PL cost benchmarks in Europe: What to expect in 2024–2025.* Retrieved from https://www.logisticsbureau.com/3pl-cost-benchmarks/

Oden Technologies. (2023). *Manufacturing assembly time benchmarks for IoT and smart devices.* Retrieved from https://oden.io/blog/assembly-time-benchmarks/

Raspberry Pi Foundation. (2024). *Raspberry Pi 4 Model B specifications.* Retrieved from https://www.raspberrypi.com/products/raspberry-pi-4-model-b/specifications/

Raspberry Pi Foundation. (2025). *Raspberry Pi product lifecycle and availability.* Retrieved from https://www.raspberrypi.com/documentation/computers/raspberry-pi.html

TÜV SÜD. (2025). *CE marking for electronic products: Process guide.* Retrieved from https://www.tuvsud.com/en/services/product-certification/ce-marking

UK Government. (2024). *Using the UKCA marking.* Retrieved from https://www.gov.uk/guidance/using-the-ukca-marking

Ventana Micro Systems / EMS Industry Association. (2024). *European EMS market report: Assembly cost and capacity benchmarks 2024.* Retrieved from https://www.emsindustry.org/european-market-report-2024

### Internal Document References

- Financial Analysis Document. (2026, March). *Financial Analysis: Reactacat 3-Year Projection & Funding Model.* Capstone project deliverable.
- Hardware Cost Analysis & Operational Budget Document. (2026, March). *Hardware Cost Analysis & Operational Budget.* Capstone project deliverable.
- Risk Analysis Document. (2026, March). *Risk Analysis: Comprehensive Risk Assessment & Mitigation Plan.* Capstone project deliverable.
- Marketing Strategy Document. (2026, March). *Marketing Strategy: Reactacat Go-to-Market & Growth Plan.* Capstone project deliverable.

---

**Document Status: COMPLETE**  
**Scope Note:** This document provides a strategic operational framework. Detailed process documentation, supplier contracts, and SOP manuals will be developed during Months 1–6 as part of pre-launch preparation.
