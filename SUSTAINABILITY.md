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
| **Laser Module** | Light source | Discrete module with standard power supply |
| **Power Supply Unit** | Device power | Standard DC barrel jack 5.5x2.1mm |
| **Housing Elements** | Component protection | 3D-replaceable sections |
| **Treat Dispenser Module** | Optional accessory | USB-C connection + magnetic mounting |

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

3. **Open specifications**
   - Housing CAD files for 3D printing (STL/STEP formats)
   - Bill of Materials (BOM) with supplier links
   - Inter-module communication protocols

### 2.2 Design for Repair

**Design decisions:**

| Anti-pattern | Our Solution | Why It Matters |
|--------------|--------------|----------------|
| Glue instead of screws | Modular M3 screw mounting | Ability to disassemble without damage |
| Proprietary power adapters | Standard USB-C power delivery | Universal charger compatibility, future-proof |
| Sealed enclosures | Magnetic/screw-on panels | Quick access to internal components |
| Soldered components | Connectors and sockets | Replacement without soldering iron |
| Encrypted firmware | Open module firmware | Independent updates and repair |

### 2.3 Spare Parts & Support

**Spare parts policy:**
- Warranty: 2 years on all components
- Post-warranty support: 7+ years of spare parts availability
- "Repair Kit" program — sets of most common spare parts at a discount
- Partnership with independent repair shops

---

## 3. Eco-Friendly Materials

### 3.1 Housing: PLA and Biodegradable Alternatives

**Primary material: PLA (Polylactic Acid)**

| Characteristic | Value |
|----------------|-------|
| **Source** | Corn starch, sugarcane |
| **Biodegradability** | Industrial composting 3-6 months (EN 13432) |
| **Home composting** | Slow decomposition (1-2 years) — not ideal |
| **Strength** | Sufficient for consumer use |
| **3D printing** | Excellent suitability for FDM printers |
| **Recycling** | Mechanical recycling into new filament |

**Why PLA:**
- **Renewable source:** does not depend on oil
- **Low carbon footprint:** production emits less CO₂
- **Local production:** ability to manufacture housings locally in each region
- **Recycling:** worn housings can be ground up and new ones printed

**Alternatives for specific needs:**

| Material | Application | Features |
|----------|-------------|----------|
| **PETG** | Parts requiring flexibility | Recycled plastic, durability |
| **Hemp Plastic** | External panels | 100% biodegradable, aesthetics |
| **Cork Composite** | Damping elements | Natural, antibacterial |
| **Recycled ABS** | Internal structural elements | Closed-loop production |

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
│  │ PLA      │──────────→│ 5-10     │──────────→│ Mechanical│
│  │ pellets  │           │ years    │           │ recycling│ │
│  └──────────┘           └──────────┘           └────┬─────┘ │
│       ↑                                             │       │
│       │                                             ↓       │
│  ┌────┴─────┐                                 ┌──────────┐ │
│  │ Biomass  │                                 │ New      │ │
│  │ (corn/   │←────────────────────────────────│ filament │ │
│  │ sugarcane│                                 └──────────┘ │
│  └──────────┘                                               │
│                                                             │
│  ┌──────────┐           ┌──────────┐           ┌──────────┐ │
│  │ Electronics│         │ Replaceable│          │ Replacement│
│  │ (standard)│───────→│ modules  │──────────→│ / repair │ │
│  └──────────┘           └──────────┘           └────┬─────┘ │
│       ↑                                             │       │
│       │                                      ┌──────┴──────┐│
│       └──────────────────────────────────────┤ Secondary   ││
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
| **Device power** | DC Barrel Jack 5.5x2.1mm | Universal, inexpensive adapters |
| **Internal module power** | JST-XH 2.54mm | DIY community standard |
| **Camera** | USB 2.0 Type-A / UVC | Plug-and-play, any compatible camera |
| **Servos** | 3-pin PWM (Futaba/JR) | Universal RC model standard |
| **Additional modules** | USB-C | Modern standard, power + data |
| **Expansion** | GPIO header (Raspberry Pi compatible) | HAT board ecosystem |
| **Connectivity** | Wi-Fi 802.11n / Ethernet RJ45 | Open standards |

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

**Recommended: Raspberry Pi Zero 2 W**

| Characteristic | Value |
|----------------|-------|
| **Architecture** | ARM Cortex-A53 (open) |
| **GPIO** | 40-pin, HAT compatible |
| **OS** | Raspberry Pi OS (Linux, open source) |
| **Community** | Millions of users, thousands of projects |
| **Replaceability** | Any SBC with compatible GPIO (Orange Pi, Banana Pi) |

**Alternatives (plug-and-play):**
- Orange Pi Zero 2W
- Banana Pi M2 Zero
- Radxa Zero

---

## 5. Circular Economy

### 5.1 Take-Back Program

**"Reactacat Forever":**
- **Trade-in:** 20% discount on new device when returning old one
- **Repair vs Replacement:** free diagnostics, transparent choice
- **Recycling:** sending worn devices for disassembly and recycling

### 5.2 Open Design

**Licensing:**
- **Housing CAD files:** CERN Open Hardware Licence v2
- **Schematics:** Creative Commons BY-SA
- **Software:** GPL v3 or MIT (TBD)

**What this enables:**
- Community can create their own modifications
- Independent manufacturers can make compatible accessories
- Device lives on even if the company ceases to exist

### 5.3 Local Production

**"Produce Where You Sell" Strategy:**

| Region | Production Approach |
|--------|---------------------|
| **Europe** | Local 3D print shops + assembly centers |
| **North America** | Partnership with local manufacturers |
| **Other markets** | Design licensing to local manufacturers |

**Benefits:**
- Reduced carbon footprint from transportation
- Support for local economy
- Faster adaptation to local regulations

---

## 6. Sustainability Technical Specifications

### 6.1 Estimated Service Life

| Component | Expected Lifespan | Extension Strategy |
|-----------|-------------------|-------------------|
| PLA housing | 5-10 years | Section replacement, 3D printing |
| Servos | 2-5 years (depending on use) | Easy replacement, <$5 |
| SBC | 5-10 years | Upgrade to newer model |
| Camera | 5+ years | USB replacement with any compatible |
| Power supply | 5-10 years | Standard adapter |
| Laser module | 10,000+ hours | Module replacement |

**Total device service life:** 10+ years with regular maintenance

### 6.2 Planned Obsolescence: Absent

**Why the device won't become obsolete:**
- AI models update via cloud (software improvement)
- Hardware compatible with open standards
- Modularity allows individual component updates
- Community can create their own improvements

### 6.3 Comparison with Competitors

| Characteristic | Reactacat | Typical Competitors |
|----------------|-----------|---------------------|
| Modularity | Full | Limited or absent |
| Repairability | Documented | Not supported |
| Spare parts | Available 7+ years | Warranty period only |
| Housing materials | PLA/biodegradable | ABS/PC (petroleum-based) |
| Standard connectors | 100% | Partially proprietary |
| Open design | Yes | No |

---

## 7. Regulatory Compliance

### 7.1 European Directives

**Right to Repair Directive (2024+):**
- ✅ Design for disassembly
- ✅ Spare parts availability 7+ years
- ✅ Repair documentation
- ✅ Software updates 5+ years

**Ecodesign Directive:**
- ✅ Low carbon footprint materials
- ✅ Recycling and reuse
- ✅ Environmental impact information

**WEEE Directive:**
- ✅ Take-back program
- ✅ Material separation
- ✅ Hazardous substance minimization

### 7.2 Certifications

**Target certifications:**
- **TCO Certified** — IT product sustainability
- **EPEAT** — electronics environmental assessment
- **Cradle to Cradle** — circular design (prospect)

---

## 8. Sustainability Marketing

### 8.1 Messaging for Users

**Key message:**
> "Reactacat is the last cat toy you'll ever buy. Repairable. Upgradable. Built to last for years."

**Key messages:**
1. **For eco-conscious:** "Made from plants, not oil"
2. **For practical users:** "Servo broken? Replacement in 5 minutes for $3"
3. **For tech enthusiasts:** "Open code, open schematics, your toy — your rules"
4. **For cost-conscious:** "10+ years of service instead of 2-3 years of planned obsolescence"

### 8.2 Transparency

**What we publish:**
- Carbon footprint of manufacturing one device
- Materials supplier map
- Recycling and waste report
- Product Lifecycle Assessment (LCA)

---

## 9. Financial Aspect

### 9.1 Cost of Sustainable Design

**Additional costs:**
- Modular architecture development: +5-10% to R&D
- Documentation and open specifications: +2-3%
- PLA vs ABS: +15-20% material cost (offset by local production)

**Savings:**
- Fewer warranty cases: -15% support costs
- Customer loyalty: +30% repeat purchases (accessories, upgrades)
- Premium positioning: +20% price

### 9.2 Sustainability Monetization Model

**Main device:**
- Sale with small margin (cover costs)

**Long-term revenue:**
- Cloud AI subscription (primary model)
- Module upgrade sales
- Spare parts and accessories
- Design licensing to local manufacturers

---

## 10. Implementation Plan

### 10.1 MVP vs Full Version

| Feature | MVP (Year 1) | Full Version (Year 2+) |
|---------|--------------|------------------------|
| Modularity | Main modules | Full modularity |
| Documentation | Basic | Complete + videos |
| CAD files | Basic housings | All parts |
| Take-back program | Pilot (EU) | Global |
| Materials | 50% PLA | 90%+ eco-friendly |
| Local production | 1 region | 3+ regions |

### 10.2 Success Metrics

**Quantitative:**
- Average device service life: >5 years
- Repair vs replacement rate: >70% repairs
- Percentage of recycled materials: >80%
- Carbon footprint reduction vs competitors: -40%

**Qualitative:**
- Accessory developer community: active
- Independent reviews: positive
- Sustainability awards: 2+ in first 3 years

---

## 11. Risks & Mitigation

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| PLA not strong enough | Medium | High | PETG for structural elements; testing |
| Users don't repair | High | Medium | Service network; video instructions; community |
| Open design → copies | Medium | Medium | Focus on AI service (not clonable) |
| Cost higher than competitors | High | Medium | Premium/sustainable marketing; TCO arguments |
| Standard parts suppliers | Low | High | Diversification; stocking key components |

---

## 12. Conclusions

Reactacat places sustainability and the right to repair at the center of product philosophy. This is not a compromise — it is a competitive advantage:

1. **Longevity** reduces total cost of ownership for the user
2. **Modularity** creates additional revenue channels for the business
3. **Openness** builds a loyal community around the product
4. **Eco-friendliness** meets growing demand and regulatory requirements
5. **Standardization** reduces supplier dependency and risks

**Next Steps:**
- [ ] Finalize CAD design with modular architecture
- [ ] Test PLA housing durability
- [ ] Develop service documentation
- [ ] Find local manufacturers for pilot launch
- [ ] Carbon footprint assessment (LCA)

---

**Document Status:** Draft v1.0  
**Author:** Clawdio (AI Research Assistant)  
**Next Review:** After design finalization
