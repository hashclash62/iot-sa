---
title: Unit 4 Notes Index
parent: Unit 4 — Industrial IoT Applications
nav_order: 3
---

# Unit 4 Notes — Study Index & README

**Unit:** Industrial IoT Applications
**Questions covered:** 22 questions

---

## File Index

| File | Topics Covered | Questions |
|------|----------------|-----------|
| `01-iiot-in-healthcare.md` | Healthcare monitoring, equipment tracking, cold chain, remote patient monitoring | Q1, Q5, Q18 |
| `02-power-plant-and-energy-management.md` | Power plant monitoring, turbine health, boiler optimization, energy management, smart metering | Q6, Q14, Q22 |
| `03-inventory-and-quality-control.md` | RFID inventory, real-time stock tracking, in-process quality monitoring, SPC, vision inspection | Q3, Q7, Q8, Q22 |
| `04-plant-safety-and-facility-management.md` | Plant safety systems, worker wearables, AR safety, VR safety training, facility management (HVAC, lighting) | Q2, Q4, Q9, Q10, Q11, Q17, Q19 |
| `05-iiot-impact-challenges-ethics.md` | IIoT benefits (OEE), deployment challenges, data-driven decisions (DIKW), ethics, security, productivity impact | Q12, Q13, Q15, Q16, Q20, Q21 |

---

## Full Syllabus Checklist

### IIoT in Healthcare
- [ ] List 5 applications of IIoT in healthcare
- [ ] Explain continuous patient monitoring system architecture
- [ ] Describe medical equipment tracking with RTLS/BLE
- [ ] Explain cold chain monitoring for vaccines and drugs
- [ ] Describe remote patient monitoring (RPM) and its impact on chronic disease management
- [ ] Analyze how IIoT improves hospital operational efficiency

### Power Plants & Energy Management
- [ ] Explain what gets monitored in a thermal power plant (boiler, turbine, generator, transformer)
- [ ] Draw the IIoT architecture for a power plant (sensors → DCS → edge → cloud → dashboard)
- [ ] Describe predictive maintenance for turbines (vibration analysis)
- [ ] Explain transformer health monitoring using DGA sensors
- [ ] Explain energy management using IIoT: smart sub-meters, analytics, demand response
- [ ] Give an example of energy savings achieved through IIoT (compressed air, scheduling, motor efficiency)

### Inventory Management & Quality Control
- [ ] Define inventory management and the IIoT problem it solves
- [ ] List 5 IIoT technologies for inventory: RFID, barcode, BLE beacons, weight sensors, computer vision
- [ ] Explain the IIoT inventory management system architecture
- [ ] List 4 benefits: real-time visibility, reduced safety stock, eliminate stockouts, shrinkage control
- [ ] Explain in-process parameter monitoring for quality
- [ ] Describe automated vision inspection with CNN
- [ ] Explain real-time SPC with IIoT (100% inspection vs sampling)
- [ ] Explain traceability and targeted recall

### Plant Safety, Security & Facility Management
- [ ] Define plant safety systems
- [ ] List safety sensor types and what each monitors
- [ ] Draw the IIoT safety system architecture
- [ ] Describe worker wearables: GPS, fall detection, personal gas, heat stress
- [ ] Explain AR applications in plant safety (hazard visualization, live data overlay, PTW, evacuation)
- [ ] Explain VR applications in safety training (fire drills, chemical spill, confined space rescue)
- [ ] Define facility management and list 5 IIoT applications
- [ ] Explain smart HVAC control with occupancy sensors (20-30% energy saving)

### IIoT Impact, Challenges & Decisions
- [ ] List 8 benefit areas of IIoT in industrial automation with typical improvement numbers
- [ ] List 5 technical challenges in IIoT deployment with solutions
- [ ] List 4 organizational challenges
- [ ] Explain data-driven decision-making at operational, tactical, and strategic levels
- [ ] Explain the DIKW model in IIoT context
- [ ] Describe 4 ethical issues: surveillance, job displacement, algorithmic accountability, data ownership
- [ ] Explain security issues specific to IIoT: safety-critical systems, supply chain attacks, data theft
- [ ] Define OEE = Availability × Performance × Quality; explain how IIoT improves each component

---

## Key Diagrams to Draw in Exam

1. **IIoT Healthcare Architecture** — wearable → hospital IoT gateway → EHR → nurse station + mobile alert + AI early warning
2. **Power Plant IIoT Architecture** — field sensors → DCS/SCADA → edge servers → cloud → dashboard/CMMS
3. **IIoT Inventory System** — RFID-tagged items → WMS + IIoT platform → ERP → dashboard
4. **IIoT Safety Architecture** — safety sensors → safety PLC/ESD + IIoT safety platform → control room + mobile alerts
5. **DIKW Model** — data → information → knowledge → wisdom (with IIoT example at each level)
6. **OEE = Availability × Performance × Quality** — show how IIoT improves each component with percentages

---

## Quick-Revision Cheat Sheet

### 5 IIoT Healthcare Applications
1. Continuous patient monitoring (wearables + bedside)
2. Medical equipment RTLS tracking (location + usage)
3. Cold chain monitoring (vaccines, blood products)
4. Smart medication dispensing
5. Remote patient monitoring (chronic disease management)

### Power Plant: What gets monitored
- Boiler: drum pressure, steam temp, feed water flow, flue gas O2
- Turbine: vibration, bearing temp, speed, exhaust temp
- Generator: stator winding temp, rotor temp, cooling water flow
- Transformer: oil DGA (dissolved gas analysis)

### IIoT Inventory Technologies
| Tech | Best for |
|---|---|
| RFID | Pallet/case tracking |
| BLE beacons | High-value movable assets |
| Weight/load sensors | Bins of small parts |
| Computer vision | No-tag item counting |

### IIoT Deployment Challenges
- Technical: legacy integration, interoperability, data volume, connectivity, cybersecurity
- Organizational: skills gap, change management, ROI uncertainty, departmental silos

### OEE Components
$$OEE = Availability \times Performance \times Quality$$
- Availability improved by: predictive maintenance reducing unplanned downtime
- Performance improved by: AI process optimization maintaining optimal speed
- Quality improved by: in-process monitoring + vision inspection

### Ethical Issues in IIoT
1. Worker surveillance/privacy
2. Job displacement
3. Algorithmic bias and accountability
4. Data ownership and vendor lock-in
