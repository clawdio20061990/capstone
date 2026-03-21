# Technology & Product Roadmap

**Document Version:** 1.0  
**Date:** March 2026  
**Scope:** Product evolution from MVP through Year 3, technical architecture decisions, and feature prioritization  
**Integration:** Builds on Product Concept, Hardware Cost Analysis, and Risk Analysis

---

## 1. Roadmap Overview

### 1.1 Development Philosophy

Reactacat follows a **platform-first, feature-second** approach. The core platform (edge AI + cloud backend + mobile app) is built for extensibility. Features are added as modules that leverage this platform.

**Key principles:**
- **Hardware is a delivery mechanism, software is the product:** AI improvements deploy to all devices via OTA updates
- **Cat-centric design:** Every feature evaluated against "does this improve the cat's experience?" first
- **Data-driven iteration:** Gameplay analytics inform feature prioritization
- **Subscription-alignment:** New features drive subscription value and retention

### 1.2 Version Timeline

| Version | Timeline | Focus | Key Deliverables |
|---------|----------|-------|------------------|
| **v0.1** | Month 1–4 | Alpha prototype | Working hardware, basic AI, internal testing |
| **v0.5** | Month 5–8 | Beta release | 50 beta units, cat behavior validation |
| **v1.0** | Month 9 | MVP launch | Poland soft launch, core feature set |
| **v1.1** | Month 11 | Stability + onboarding | Bug fixes, setup UX improvements |
| **v1.2** | Month 13 | Enhanced treat modes | Advanced treat scheduling, subscription tiering |
| **v2.0** | Month 18 | Custom PCB platform | Cost reduction, performance improvement |
| **v2.1** | Month 21 | Multi-cat support | Households with 2+ cats |
| **v2.5** | Month 24 | EU + UK expansion features | Localization, regional compliance |
| **v3.0** | Month 30 | Advanced AI modes | Predictive scheduling, health insights |

---

## 2. Hardware Roadmap

### 2.1 Platform Evolution

**Phase 1: Raspberry Pi 4B (Months 1–12, 1,200 units — Poland Only)**
- **Processor:** Broadcom BCM2711, quad-core Cortex-A72 @ 1.5GHz
- **RAM:** 2GB LPDDR4 (sufficient for edge inference)
- **Camera:** OV5647 5MP CSI module
- **Connectivity:** Built-in WiFi 5 + BT 5.0
- **Power:** USB-C 5V 3A

**Rationale:** Proven platform for Poland soft launch. Higher BOM cost (€38–42/unit) acceptable for market validation before hardware NRE commitment.

**Phase 2: Custom PCB (Months 18–30, 6,500+ units — EU Expansion)**} } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ] } ]
- **Processor:** Rockchip RK3566 or equivalent (quad-core Cortex-A55 + Mali-G52 GPU)
- **NPU:** 1 TOPS AI accelerator for on-device inference
- **RAM:** 1GB LPDDR4 (soldered)
- **Storage:** 8GB eMMC (soldered, replaces SD card)
- **Camera:** IMX219 8MP or OV5647 (MIPI CSI-2)
- **Connectivity:** WiFi 6 + BT 5.2 module
- **Power:** USB-C, integrated voltage regulation

**Rationale:** 30–35% cost reduction, better thermal performance, purpose-built for cat detection workload. NPU enables more sophisticated on-device AI.

### 2.2 Industrial Design Evolution

| Version | Enclosure | Key Changes |
|---------|-----------|-------------|
| **v1.0** | Injection molded ABS, 2-piece clamshell | Initial design, 150mm × 120mm × 80mm |
| **v1.2** | Same + treat dispenser module | Magnetic attachment for optional treat dispenser |
| **v2.0** | Redesigned for custom PCB | Smaller footprint (120mm × 100mm × 70mm), improved thermal design |
| **v2.5** | Color variants | White (standard), gray, limited edition colors |

### 2.3 Accessory Roadmap

| Accessory | Timeline | Description | Business Model |
|-----------|----------|-------------|----------------|
| **Treat Dispenser Module** | Month 11 | Motorized treat dispenser, compatible with standard kibble | Bundled with Premium/Ultra subscription; €25 standalone |
| **Replacement Servo Kit** | Month 12 | User-replaceable servo pair | €15 accessory, reduces warranty costs |
| **Wall Mount** | Month 14 | Adjustable wall bracket for elevated positioning | €12 accessory |
| **Travel Case** | Month 18 | Hard case for device + accessories | €20 accessory |
| **Extended Warranty** | Month 9 | 3-year warranty extension | €29 one-time |

---

## 3. Software & AI Roadmap

### 3.1 Edge AI (On-Device)

**v0.1 – Basic Detection (Month 4)**
- Cat detection using MobileNetV2 SSD (lightweight, RPi-optimized)
- Bounding box tracking across frames
- Simple movement patterns (circle, zigzag, random)

**v1.0 – Adaptive Play (Month 9)**
- Cat engagement state detection (chasing / stalking / disengaged)
- Session-based adaptation (speed, pattern type based on cat response)
- Multi-cat detection (track up to 2 cats, play with most engaged)

**v1.2 – Enhanced Treat Modes (Month 13)**
- Advanced "catch" detection with configurable reward timing
- Treat scheduling and portion control
- Multi-pattern reward sequences

**v2.0 – Enhanced Inference (Month 18)**
- Migration to custom PCB with NPU
- Pose estimation (cat body position, not just bounding box)
- Predictive movement (anticipate cat trajectory)

**v2.5 – Personality Profiles (Month 24)**
- Cat "personality" classification (hunter, stalker, sprinter)
- Breed-specific adjustments (if applicable)
- Age-appropriate play (kitten vs. adult vs. senior modes)

**v3.0 – Predictive AI (Month 30)**
- Optimal play time prediction (when cat is most receptive)
- Activity pattern learning (daily/weekly rhythms)
- Health indicators (activity level changes as early warning)

### 3.2 Cloud Backend

**v0.1 – Basic Pipeline (Month 4)**
- Gameplay log ingestion (position data, timestamps)
- Simple per-cat model storage
- Manual model retraining (weekly batch jobs)

**v1.0 – Automated Retraining (Month 9)**
- Triggered retraining after each gameplay session
- A/B testing framework (compare model variants)
- Model versioning and rollback capability

**v1.5 – Analytics Platform (Month 12)**
- Engagement dashboards for users
- Aggregate analytics for product team
- Anomaly detection (device malfunction, unusual cat behavior)

**v2.0 – Scale Architecture (Month 18)**
- Multi-region deployment (EU-West, EU-Central)
- Edge caching for model distribution
- Real-time inference pipeline for advanced features

**v3.0 – Intelligence Layer (Month 30)**
- Cross-cat learning (anonymized patterns improve all models)
- Predictive health analytics
- Integration APIs (veterinary platforms, pet insurance)

### 3.3 Mobile Application

**v1.0 – Core App (Month 9)**
- Device setup and WiFi configuration
- Live video streaming (local network)
- Basic gameplay stats (daily play time, sessions)
- Subscription management

**v1.1 – Enhanced UX (Month 11)**
- Improved onboarding flow
- Push notifications ("Your cat played 15 minutes today!")
- Troubleshooting wizard

**v1.2 – Enhanced Treat Control (Month 13)**
- Manual treat dispensing
- Treat schedule configuration
- Treat inventory tracking

**v2.0 – Social Features (Month 18)**
- Share gameplay clips
- Community leaderboards (most active cat, longest play session)
- Tips and educational content

**v2.5 – Multi-Device (Month 22)**
- Multiple Reactacat devices per household
- Multi-cat profile management
- Per-cat analytics

**v3.0 – Health Integration (Month 30)**
- Activity trend reports
- Veterinary export (PDF summary for vet visits)
- Integration with pet health apps

---

## 4. Feature Prioritization Framework

### 4.1 Prioritization Matrix

Features evaluated on two axes:
- **User Value:** Impact on cat engagement and owner satisfaction
- **Business Value:** Impact on subscription conversion, retention, and differentiation

| Quadrant | Priority | Example Features |
|----------|----------|------------------|
| **High User + High Business** | Must-have | Adaptive AI, treat dispenser, multi-cat support |
| **High User + Low Business** | Should-have | Advanced scheduling, health insights |
| **Low User + High Business** | Should-have | Referral program integration, social sharing |
| **Low User + Low Business** | Won't-have (now) | Voice control, third-party smart home integration |

### 4.2 MVP Feature Set (v1.0)

**Must-have for launch:**
- Autonomous AI-driven laser play
- Cat detection and tracking
- Treat dispenser module (completes hunting sequence — addresses laser frustration concern)
- Cloud-based model retraining
- Mobile app (setup, streaming, stats)
- Basic subscription tier (€3/month)

**Explicitly excluded from MVP:**
- Multi-cat optimization (detects multiple, plays with one)
- Two-way audio
- Video recording/cloud storage
- Advanced scheduling UI

**Rationale:** Core value proposition is autonomous intelligent play. Everything else is additive. Launching with a focused feature set reduces complexity and accelerates time-to-market.

---

## 5. Technical Debt & Architecture Decisions

### 5.1 Conscious Technical Debt

| Area | Debt | Rationale | Payoff Timeline |
|------|------|-----------|-----------------|
| **Cloud costs** | Single-region AWS (eu-central-1) | Speed to market | Month 15 (multi-region) |
| **AI model** | Rule-based fallback patterns | Ensure play even if AI fails | Month 11 (confidence-based removal) |
| **Mobile app** | Single-platform (iOS first) | Target demographic (premium cat owners, €60K+ income) skews iOS despite Android's ~70% overall market share in Poland (StatCounter, 2025). Cross-platform (React Native/Flutter) evaluation for v1.1 | Month 11 (Android) |
| **Firmware OTA** | Basic update mechanism | Functional for launch | Month 12 (robust rollback, staged rollout) |

### 5.2 Architecture Decisions

**Decision 1: Edge-first AI vs. Cloud AI**
- **Chosen:** Edge-first with cloud retraining
- **Rationale:** Latency critical for laser play; privacy (no video to cloud); offline functionality
- **Trade-off:** Limited compute on device; model size constraints

**Decision 2: Proprietary cloud vs. B2B platform**
- **Chosen:** Proprietary cloud (Reactacat-managed)
- **Rationale:** Full control over AI improvement cycle; subscription revenue; data moat
- **Trade-off:** Higher infrastructure cost; operational burden

**Decision 3: Closed platform vs. Open ecosystem**
- **Chosen:** Closed platform as base strategy, with selective openness roadmap for Phase 3+
- **Rationale:** Focus on core product quality and security; API requires support burden and documentation; closed platform protects AI competitive advantage
- **Future:** Open-source hardware documentation and selective API access planned for Phase 3+ as community development initiative. Health data API for veterinary integration (v3.0). Housing CAD files released for repair purposes under Creative Commons BY-SA.

---

## 6. Research & Development Pipeline

### 6.1 Active R&D Areas

| Area | Status | Timeline | Business Case |
|------|--------|----------|---------------|
| **Cat emotion detection** | Research | Year 2–3 | Deeper personalization, health indicators |
| **Predictive health analytics** | Research | Year 2–3 | Veterinary partnerships, premium subscription tier |
| **Alternative play modalities** | Concept | Year 3+ | Product line extension (feather wand, ball launcher) |
| **B2B veterinary platform** | Concept | Year 3+ | B2B revenue stream, clinical validation |

### 6.2 Patent Strategy

| Invention | Status | Filing Timeline | Jurisdiction |
|-----------|--------|-----------------|--------------|
| **Adaptive laser play algorithm** | Provisional — planned for filing at prototype completion (Month 4-5) | Month 12 (non-provisional) | EU, US |
| **Treat completion mechanism** | Drafting — planned for filing Month 9 | Month 15 | EU, US |
| **Cat engagement scoring method** | Research | Year 2 | TBD |

---

## 7. Platform Extensibility

### 7.1 Future Product Lines

The Reactacat platform (edge AI + cloud + mobile) is designed to support additional products:

| Product | Concept | Timeline | Synergy |
|---------|---------|----------|---------|
| **Reactacat Mini** | Lower-cost version, smaller form factor, basic random play (no AI) | Year 3 | Brand extension, entry-level market |
| **Reactacat Pro** | Larger device, multiple laser points, multi-room coverage | Year 3+ | Premium segment |
| **Reactadog** | Canine-optimized version, different play patterns | Year 4+ | Platform leverage, new market |
| **Reactabird / Reactasmall** | Small pet version (birds, rabbits) | Concept only | Platform extension |

### 7.2 B2B Opportunities

| Segment | Use Case | Requirements | Timeline |
|---------|----------|--------------|----------|
| **Veterinary clinics** | Enrichment for boarded cats | Robust design, cleaning protocols, bulk pricing | Year 2 |
| **Cat cafes** | Customer entertainment, cat welfare | High durability, public liability coverage | Year 2 |
| **Animal shelters** | Enrichment for resident cats | Non-profit pricing, donation program | Year 2 |
| **Pet hotels** | Premium boarding amenity | Integration with booking systems | Year 3 |

---

## 8. Success Metrics by Phase

### 8.1 Technical Metrics

| Metric | v1.0 Target | v2.0 Target | v3.0 Target |
|--------|-------------|-------------|-------------|
| **Cat detection accuracy** | >90% | >95% | >97% |
| **Engagement improvement vs. random** | >15% | >25% | >35% |
| **Model update latency** | <5 min | <2 min | Real-time |
| **Device uptime** | >99% | >99.5% | >99.9% |
| **OTA update success rate** | >95% | >98% | >99% |

### 8.2 Product Metrics

| Metric | v1.0 Target | v2.0 Target | v3.0 Target |
|--------|-------------|-------------|-------------|
| **Daily active users (DAU)** | 60% of installed base | 70% | 75% |
| **Average session duration** | 8 minutes | 10 minutes | 12 minutes |
| **Sessions per day** | 2.5 | 3.0 | 3.5 |
| **Subscription conversion** | 50% | 55% | 60% |
| **Monthly churn** | <5% | <4% | <3% |

---

## 9. Resource Allocation

### 9.1 Engineering Team Growth

| Role | Year 1 | Year 2 | Year 3 |
|------|--------|--------|--------|
| **CTO / Co-founder** | 1 | 1 | 1 |
| **Software Engineer (full-stack)** | 1 | 1 | 2 |
| **ML Engineer (part-time contractor)** | — | Part-time | 1 |
| **Hardware Engineer (part-time contractor)** | — | Part-time | 1 |
| **Total Engineering** | **2** | **3** | **5** |

### 9.2 R&D Budget

| Category | Year 1 | Year 2 | Year 3 |
|----------|--------|--------|--------|
| **Cloud infrastructure** | €18K | €45K | €120K |
| **Hardware prototyping** | €15K | €25K | €40K |
| **Third-party services** | €5K | €10K | €15K |
| **Patent & IP** | €8K | €5K | €10K |
| **Total R&D** | **€46K** | **€85K** | **€185K** |

---

## References

- Product Concept Document. (2026, March). *Reactacat — Product Concept Documentation.*
- Hardware Cost Analysis & Operational Budget Document. (2026, March). *Hardware Cost Analysis & Operational Budget.*
- Risk Analysis Document. (2026, March). *Risk Analysis: Comprehensive Risk Assessment & Mitigation Plan.*
- Marketing Strategy Document. (2026, March). *Marketing Strategy: Reactacat Go-to-Market & Growth Plan.*

---

**Document Status: COMPLETE**  
**Scope:** Strategic technology and product roadmap from MVP through Year 3, including hardware evolution, AI capabilities, mobile app features, and platform extensibility.
