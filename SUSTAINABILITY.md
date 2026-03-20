# Reactacat - Sustainability & Right to Repair Strategy

**Last Updated:** March 2026  
**Status:** Concept Stage - Design for Sustainability

---

## Executive Summary

Reactacat embraces sustainable manufacturing and the right to repair as fundamental design principles. Instead of planned obsolescence and proprietary solutions, we are designing a device that will last for years, is easily repairable, and minimizes environmental impact at all stages of its lifecycle.

---

## 1. Modular Architecture

### 1.1 Modularity Principle

**Concept:** The device consists of independent modules, each of which can be replaced individually without replacing the entire device.

#### Main Modules:

| Module | Function | Ease of Replacement |
|--------|----------|---------------------|
| **Main Board (SBC)** | Computing, AI inference | Plug-and-play via standard GPIO/USB |
| **Camera Module** | Video capture, tracking | USB/UVC standard |
| **Servos (2x)** | Laser movement on X/Y axes | Standard 3-pin PWM servos |
| **Laser Module** | Class 3R (5mW) light source with optical filter | Discrete module with standard power supply |
| **Power Supply Unit** | Device power | Standard USB-C power delivery |
| **Housing Elements** | Component protection | Injection-molded ABS (replaceable sections) |
| **Treat Dispenser Module** | Treat reward system (included in MVP) | USB-C connection + magnetic mounting |

#### Benefits of Modularity:

**For the user:**
- Repair a specific component instead of discarding the device
- Upgrade individual modules (e.g., more powerful camera)
- Ability to reconfigure for different spaces

**For the business:**
- Reduced warranty service costs
- Additional revenue from spare parts and module sales
- Positive brand image showing care for customers

**For the environment:**
- Reduced electronic waste (e-waste)
- Problem localization — replace one module instead of the whole device
- Easy component sorting for secondary recycling

---

## 2. Right to Repair

### 2.1 Documentation & Openness

**What we provide:**

1. **Complete disassembly diagrams**
   - Step-by-step instructions with photos
   - Identification of every component
   - Required tools (standard screwdrivers, plastic spudgers)

2. **Service documentation**
   - Diagnostic error codes
   - Troubleshooting tables
   - Preventive maintenance recommendations

3. **Specifications**
   - Housing CAD files for 3D printing replacement parts (STL/STEP formats)
   - Bill of Materials (BOM) with supplier links
   - Inter-module communication protocols
   - Open-source hardware documentation and selective API access planned for Phase 3+ as community development initiative

### 2.2 Design for Repair

**Design decisions:**

| Anti-pattern | Our Solution | Why It Matters |
|--------------|--------------|----------------|
| Glue instead of screws | Modular M3 screw mounting | Ability to disassemble without damage |
| Proprietary power adapters | Standard USB-C power delivery | Universal charger compatibility, EU compliant, future-proof |
| Sealed enclosures | Magnetic/screw-on panels | Quick access to internal components |
| Soldered components | Connectors and sockets | Replacement without soldering iron |
| Encrypted firmware | Documented module firmware with update capability | Independent updates and repair |

### 2.3 Spare Parts & Support

**Spare parts policy:**
- Warranty: 2 years on all components
- Post-warranty support: Target 7+ years of spare parts availability. This aspiration is supported by: (a) use of widely available standard components (SG90 servos, USB cameras, Raspberry Pi ecosystem), reducing single-supplier dependency; (b) design documentation enabling third-party manufacturing of replacement parts; and (c) a dedicated spare parts inventory reserve budgeted from Year 2 onwards.
- "Repair Kit" program — sets of most common spare parts at a discount
- Partnership with independent repair shops

---

## 3. Eco-Friendly Materials

### 3.1 Housing: ABS with Sustainability Roadmap

**Production material: ABS (Acrylonitrile Butadiene Styrene) — Injection Molded**

Early prototypes used PLA via 3D printing for rapid iteration and low-volume testing. Production units use injection-molded ABS, which offers superior impact resistance, thermal stability, and manufacturing scalability required for a consumer electronics product. We plan to evaluate recycled ABS and bio-based alternatives (e.g., bio-based PA, PHA composites) for future production versions.

| Characteristic | Value |
|----------------|-------|
| **Source** | Petroleum-based polymer |
| **Biodegradability** | Not biodegradable; fully recyclable via mechanical recycling (plastic type code 7/ABS) |
| **Strength** | Excellent impact resistance, suitable for consumer electronics |
| **Manufacturing** | Injection molding — cost-effective at scale |
| **Recycling** | Mechanical recycling into new ABS products; take-back program ensures proper collection |

**Sustainability roadmap for housing materials:**

| Phase | Material | Rationale |
|-------|----------|-----------|
| **Prototyping** | PLA (3D printed) | Rapid iteration, low-volume, corn-based feedstock |
| **Production v1.0** | Virgin ABS (injection molded) | Proven durability, manufacturing scalability |
| **Production v2.0+** | Recycled ABS / bio-based alternatives | Evaluate recycled ABS suppliers; test bio-based PA or PHA composites for structural integrity |

**Alternatives under evaluation for specific components:**

| Material | Application | Features |
|----------|-------------|----------|
| **PETG** | Parts requiring flexibility | Recyclable, good durability |
| **Recycled ABS** | Housing (future production runs) | Closed-loop production, reduced virgin material |
| **Cork Composite** | Damping elements | Natural, antibacterial |

### 3.2 Packaging

**Zero-waste approach:**

- **Box:** Recycled cardboard, soy-based printing ink
- **Protection:** Corn-based packing material (dissolves in water) instead of foam
- **Bags:** Compostable PLA bags for small components
- **Instructions:** QR code to electronic version, minimal paper printing

### 3.3 Material Lifecycle

```
┌─────────────────────────────────────────────────────────────┐
│                    REACTACAT LIFECYCLE                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  MANUFACTURING           USAGE                END OF LIFE   │
│                                                             │
│  ┌──────────┐           ┌──────────┐           ┌──────────┐ │
│  │ ABS      │──────────→│ 5-10     │──────────→│ Mechanical│ │
│  │ pellets  │           │ years    │           │ recycling │ │
│  └──────────┘           └──────────┘           └────┬─────┘ │
│       ↑                                             │       │
│       │                                             ↓       │
│  ┌────┴─────┐                                 ┌──────────┐  │
│  │ Recycled │                                 │ Recycled  │  │
│  │ ABS      │←────────────────────────────────│ granulate │  │
│  │ (future) │                                 └──────────┘  │
│  └──────────┘                                               │
│                                                             │
│  ┌──────────┐           ┌──────────┐           ┌──────────┐ │
│  │ Electronics│         │ Replaceable│          │ Replacement│
│  │ (standard)│───────→  │ modules  │──────────→│ / repair │ │
│  └──────────┘           └──────────┘           └────┬─────┘ │
│       ↑                                             │       │
│       │                                      ┌──────┴──────┐│
│       └──────────────────────────────────────┤ WEEE-       ││
│                                              │ compliant   ││
│                                              │ recycling   ││
│                                              │ (collection ││
│                                              │ points)     ││
│                                              └─────────────┘│
└─────────────────────────────────────────────────────────────┘
```

---

## 4. Component Standardization

### 4.1 Philosophy: "No Proprietary Connectors"

**Principle:** Every connector, port, and interface is an open standard available to any manufacturer.

### 4.2 Electrical Interfaces

| Purpose | Standard | Why This Choice |
|---------|----------|-----------------|
| **Device power** | USB-C 5V 3A | Modern universal standard, EU-mandated direction, supports power + data |
| **Internal module power** | JST-XH 2.54mm | DIY community standard |
| **Camera** | MIPI CSI-2 (RPi compatible) / USB UVC | Plug-and-play, ecosystem compatibility |
| **Servos** | 3-pin PWM (Futaba/JR) | Universal RC model standard |
| **Additional modules** | USB-C | Modern standard, power + data |
| **Expansion** | GPIO header (Raspberry Pi compatible) | HAT board ecosystem |
| **Connectivity** | Wi-Fi 802.11ac / Ethernet RJ45 | Open standards |

### 4.3 Mechanical Standards

**Fastening:**
- All screws: **M3** (metric system, standard for electronics)
- Mounting hole spacing: multiples of **10mm** (modular grid)
- Board mounting: **M3 standoffs** standard height

**Servos:**
- Standard size: **9g micro servo** (SG90 or equivalents)
- Alternative: **MG90S** (metal gears for durability)
- Rotation angle: 180° (standard) or 360° (continuous rotation)
- Power supply: 4.8-6V (compatible with 5V SBC logic)

**Advantages of standard servos:**
- Availability: <$3 per unit anywhere in the world
- Easy replacement: only 3 wires
- Reliability: millions of identical actuators in production
- Repairability: mechanisms well understood

### 4.4 Computing Platform

**Phase 1: Raspberry Pi 4B**

| Characteristic | Value |
|----------------|-------|
| **Architecture** | ARM Cortex-A72 (quad-core @ 1.5GHz) |
| **RAM** | 2GB LPDDR4 |
| **GPIO** | 40-pin, HAT compatible |
| **OS** | Raspberry Pi OS (Linux, open source) |
| **Connectivity** | Built-in Wi-Fi 5 + BT 5.0 |
| **Power** | USB-C 5V 3A |
| **Community** | Millions of users, thousands of projects |
| **Replaceability** | Any SBC with compatible GPIO (Orange Pi, Banana Pi) |

**Rationale:** Proven platform with extensive ecosystem and sufficient compute for real-time computer vision with MobileNetV2 SSD. Quad-core A72 and 2GB RAM provide comfortable headroom for edge AI inference. Higher BOM cost (vs. lighter SBCs) accepted for development speed and reliability during initial production.

**Phase 2 (Month 18+): Custom PCB** based on Rockchip RK3566 or equivalent, achieving 30-35% cost reduction at scale.

---

## 5. Circular Economy

### 5.1 Take-Back Program

**"Reactacat Forever":**
- **Trade-in:** 20% discount on new device when returning old one
- **Repair vs Replacement:** free diagnostics, transparent choice
- **Recycling:** WEEE-compliant collection and disassembly of returned devices through certified e-waste partners

### 5.2 Platform Strategy & Openness

**Base strategy: Closed platform** with proprietary AI models and cloud services, ensuring quality control, security, and consistent user experience.

**Future openness roadmap (Phase 3+):**
- Open-source hardware documentation and selective API access planned as community development initiative
- Housing CAD files for replacement parts under Creative Commons BY-SA
- Health data API for veterinary integration
- Third-party accessory compatibility specification

**Licensing (planned for Phase 3+):**
- **Housing CAD files:** Creative Commons BY-SA (for repair/replacement purposes)
- **Hardware schematics:** Under evaluation — CERN Open Hardware Licence v2 considered
- **Software/AI models:** Proprietary (core competitive advantage)

### 5.3 Local Production

**"Produce Where You Sell" Strategy (Phase 2+):**

| Region | Production Approach |
|--------|---------------------|
| **Europe** | Contract manufacturing (injection molding) + assembly centers |
| **North America** | Partnership with local manufacturers (Phase 3+) |
| **Other markets** | Design licensing to local manufacturers (Phase 3+) |

**Benefits:**
- Reduced carbon footprint from transportation
- Support for local economy
- Faster adaptation to local regulations

---

## 6. Sustainability Technical Specifications

### 6.1 Estimated Service Life

| Component | Expected Lifespan | Extension Strategy |
|-----------|-------------------|-------------------|
| ABS housing | 5-10 years | Section replacement; CAD files available for 3D printing custom replacements |
| Servos | 2-5 years (depending on use) | Easy replacement, <$5 |
| SBC (Raspberry Pi 4B) | 5-10 years | Upgrade to newer compatible model |
| Camera | 5+ years | CSI/USB replacement with any compatible module |
| Power supply | 5-10 years | Standard USB-C adapter |
| Laser module | 10,000+ hours | Module replacement |

**Total device service life:** 10+ years with regular maintenance

### 6.2 Planned Obsolescence: Absent

**Why the device won't become obsolete:**
- AI models update via cloud (software improvement)
- Hardware compatible with open standards
- Modularity allows individual component updates
- Community can create compatible accessories and modifications (Phase 3+)

### 6.3 Comparison with Competitors

| Characteristic | Reactacat | Petcube Play 2 | PetSafe Bolt |
|----------------|-----------|-----------------|--------------|
| Modularity | Full modular design | Limited (sealed unit) | None |
| Repairability | Documented disassembly | Not officially supported | Not supported |
| Spare parts | Target 7+ years | Warranty period only | Warranty period only |
| Housing materials | ABS (recycled ABS planned) | ABS/PC | ABS/PC |
| Standard connectors | 100% open standards | Proprietary power | Proprietary |
| Open design files | Planned for Phase 3+ | No | No |

*Sources: Product teardowns and official specifications from Petcube (petcube.com) and PetSafe (petsafe.com) as of March 2026.*

---

## 7. Regulatory Compliance

### 7.1 European Directives

**EU Right to Repair Regulation (adopted 2024, member state transposition by 2026):**
- ✅ Design for disassembly
- ✅ Spare parts availability target: 7+ years
- ✅ Repair documentation
- ✅ Software updates 5+ years

*Reference: Directive (EU) 2024/1799 on common rules promoting the repair of goods*

**Ecodesign for Sustainable Products Regulation (ESPR):**
- ✅ Low carbon footprint materials roadmap
- ✅ Recycling and reuse design
- ✅ Environmental impact information (Digital Product Passport readiness)

**WEEE Directive (2012/19/EU):**
- ✅ Take-back program
- ✅ Material separation design
- ✅ Hazardous substance minimization
- ✅ Producer registration in each EU market

*Reference: Directive 2012/19/EU on waste electrical and electronic equipment*

### 7.2 Product Safety Standards

**Target certifications:**
- **CE marking** — mandatory for EU market
- **IEC 60825-1** — laser safety classification (Class 3R with optical filter ensuring Class 1 conditions at user distance)
- **RoHS / REACH** — restricted substances and chemical safety compliance
- **RED Directive** — radio equipment (Wi-Fi/Bluetooth)

*Reference: IEC 60825-1:2014 "Safety of laser products"*

### 7.3 Aspirational Certifications (Year 2+)

- **TCO Certified** — IT product sustainability
- **EPEAT** — electronics environmental assessment

---

## 8. Sustainability Marketing

### 8.1 Messaging for Users

**Key message:**
> "Reactacat is the last cat toy you'll ever buy. Repairable. Upgradable. Built to last for years."

**Key messages:**
1. **For eco-conscious:** "Designed for repair, not replacement — with a recycling take-back program"
2. **For practical users:** "Servo broken? Replacement in 5 minutes for $3"
3. **For tech enthusiasts:** "Standard components, documented design, upgrade-friendly"
4. **For cost-conscious:** "10+ years of service instead of 2-3 years of planned obsolescence"

### 8.2 Transparency

**What we plan to publish:**
- Carbon footprint estimate for manufacturing one device
- Materials supplier information
- Recycling and waste report (once production begins)
- Product Lifecycle Assessment (LCA) — planned for Year 2

---

## 9. Financial Aspect

### 9.1 Cost of Sustainable Design

**Additional costs:**
- Modular architecture development: estimated +5-10% to R&D (based on comparable IoT product development)
- Documentation and specifications: +2-3%
- ABS vs. cheaper materials: minimal premium; recycled ABS evaluation may add 10-15% to material cost in future

**Expected savings (projected, based on industry benchmarks for modular consumer electronics):**
- Fewer warranty cases through self-repair: estimated -10-15% support costs
- Customer loyalty from repairability: higher repeat purchase rate for accessories and upgrades
- Premium positioning: sustainable design supports €150 price point vs. commodity alternatives

*Note: Specific financial projections are detailed in the Financial Analysis document.*

### 9.2 Sustainability Monetization Model

**Main device:**
- Sale with margin (see Financial Analysis for detailed unit economics)

**Long-term revenue:**
- Cloud AI subscription (primary recurring model)
- Module upgrade sales
- Spare parts and accessories
- Design licensing to local manufacturers (Phase 3+)

---

## 10. Implementation Plan

### 10.1 MVP vs Full Version

| Feature | MVP (Year 1) | Full Version (Year 2+) |
|---------|--------------|------------------------|
| Modularity | Main modules (servo, camera, SBC, laser, treat dispenser) | Full modularity with expansion port |
| Documentation | Basic disassembly guide | Complete guide + video tutorials |
| CAD files | Internal use | Repair-use release (Phase 3+) |
| Take-back program | Pilot (Poland) | EU-wide |
| Materials | ABS injection molded | Evaluate recycled ABS |
| Local production | Contract manufacturing (1 region) | 3+ regions |

### 10.2 Success Metrics

**Quantitative:**
- Average device service life: >5 years
- Repair vs replacement rate: >70% repairs (target)
- Percentage of recyclable materials: >90%
- WEEE-compliant end-of-life collection rate: >30% by Year 3

**Qualitative:**
- Accessory developer community (Phase 3+): active
- Independent reviews: positive on repairability
- Sustainability recognition: target 1-2 industry awards in first 3 years

---

## 11. Risks & Mitigation

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| ABS housing durability issues | Low | Medium | Proven material for consumer electronics; extensive testing in prototype phase |
| Users don't repair | High | Medium | Service network; video instructions; community; repair kit program |
| Closed platform limits community | Medium | Medium | Phase 3+ openness roadmap addresses long-term; core product value not dependent on community |
| Cost higher than competitors | High | Medium | Premium/sustainable marketing; TCO arguments; subscription value |
| Standard parts supplier disruption | Low | High | Multiple supplier qualification; 3-month component buffer |

---

## 12. Conclusions

Reactacat places sustainability and the right to repair at the center of product philosophy. This is not a compromise — it is a competitive advantage:

1. **Longevity** reduces total cost of ownership for the user
2. **Modularity** creates additional revenue channels for the business
3. **Closed platform with future openness** balances quality control with community potential
4. **Sustainability roadmap** meets growing demand and regulatory requirements (WEEE, Right to Repair, ESPR)
5. **Standardization** reduces supplier dependency and risks

**Next Steps:**
- [ ] Finalize CAD design with modular architecture
- [ ] Test ABS housing durability (prototype phase with PLA, production with ABS)
- [ ] Develop service documentation
- [ ] Find contract manufacturer for injection molding (Poland/EU)
- [ ] Carbon footprint assessment (LCA) — planned for Year 2

---

## References

1. Directive 2012/19/EU of the European Parliament and of the Council on waste electrical and electronic equipment (WEEE). *Official Journal of the European Union*, L 197/38.
2. IEC 60825-1:2014. *Safety of laser products — Part 1: Equipment classification and requirements*. International Electrotechnical Commission.
3. Directive (EU) 2024/1799 on common rules promoting the repair of goods. *Official Journal of the European Union*.
4. Regulation (EU) 2024/1781 establishing a framework for setting ecodesign requirements for sustainable products (ESPR). *Official Journal of the European Union*.
5. EN 13432:2000. *Packaging — Requirements for packaging recoverable through composting and biodegradation*. European Committee for Standardization. *(Applicable to PLA prototype packaging only.)*
6. FEDIAF (European Pet Food Industry). (2024). *Annual Report: European Facts & Figures*.

---

**Document Status:** Draft v2.0  
**Author:** Clawdio (AI Research Assistant)  
**Next Review:** After design finalization
