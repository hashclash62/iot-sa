---
title: Unit 3 Notes Index
parent: Unit 3 — CPS, Sensors, AR/VR, AI & PLM
nav_order: 3
---

# Unit 3 Notes — Study Index & README

**Unit:** Cyber-Physical Systems, Advanced Sensing, AR/VR, AI/Big Data, PLM
**Questions covered:** 29 questions

---

## File Index

| File | Topics Covered | Questions |
|------|----------------|-----------|
| `01-cyber-physical-systems.md` | CPS definition, 5C architecture, feedback loop, CPS vs automation, smart factory example, challenges | Q1, Q8, Q13, Q23, Q25, Q27, Q29 |
| `02-next-generation-sensors.md` | Next-gen sensor types, data accuracy, real-time monitoring, sensor data fusion | Q2, Q7, Q12, Q14, Q22 |
| `03-ar-and-vr-in-industry.md` | AR/VR definitions, industrial maintenance (AR), training (VR), Boeing example | Q3, Q4, Q5, Q6, Q11, Q18, Q19, Q26 |
| `04-ai-bigdata-advanced-analytics.md` | AI roles in CPS, Big Data 5 Vs, ML techniques, advanced analytics, AI+Big Data decision-making | Q15, Q20, Q21, Q24, Q28 |
| `05-plm-and-collaborative-platforms.md` | PLM lifecycle, smart manufacturing integration, collaborative platforms, data sharing | Q9, Q10, Q16, Q17 |

---

## Full Syllabus Checklist

### CPS Fundamentals
- [ ] Define Cyber-Physical Systems (CPS)
- [ ] List the 5C architecture layers (Connection, Conversion, Cyber, Cognition, Configuration)
- [ ] Draw the CPS feedback loop (sense → compute → actuate → monitor)
- [ ] Distinguish CPS from traditional automation
- [ ] Apply CPS to an industrial automation problem
- [ ] Design a CPS architecture for a smart factory
- [ ] Explain CPS challenges (interoperability, security, latency, complexity)

### Next-Generation Sensors
- [ ] Define next-generation sensors
- [ ] List 6 sensor types: MEMS, smart, wireless, multifunctional, nano, biosensors
- [ ] Explain how next-gen sensors improve data accuracy
- [ ] Describe real-time monitoring applications in smart industry
- [ ] Explain 3 levels of sensor data fusion (raw, feature, decision)
- [ ] Name 4 fusion techniques: Kalman filter, Bayesian, Dempster-Shafer, ML-based

### AR & VR in Industry
- [ ] Define Augmented Reality (AR) and Virtual Reality (VR)
- [ ] Distinguish AR from VR in an industrial context (comparison table)
- [ ] Explain AR-based industrial maintenance workflow (step-by-step)
- [ ] Describe AR applications: maintenance guidance, remote expert, assembly, quality inspection
- [ ] Describe VR applications: operator training, safety drills, design review, commissioning
- [ ] Propose a complete AR-based industrial maintenance system

### AI & Big Data in CPS
- [ ] State the 5 Vs of Big Data (Volume, Velocity, Variety, Veracity, Value)
- [ ] Describe Big Data infrastructure: ingestion → storage → analytics
- [ ] Explain 3 AI roles in CPS: anomaly detection, predictive modeling, process optimization
- [ ] Describe 5 AI techniques: supervised, unsupervised, RL, computer vision, NLP
- [ ] Explain how AI + Big Data enable closed-loop CPS decision-making
- [ ] Describe advanced analytics: time-series, FFT spectral, digital twin, RCA analytics

### PLM & Collaborative Platforms
- [ ] Define PLM and its 4 lifecycle stages
- [ ] List core PLM capabilities (PDM, BOM, change mgmt, config mgmt, workflow)
- [ ] Explain PLM in smart manufacturing (CAD→CAM, digital twin, as-built tracking, IIoT feedback)
- [ ] Define collaborative platforms and their types
- [ ] Apply collaborative platform to enhance communication in manufacturing
- [ ] Explain PLM for product development and maintenance (digital thread, SLM)

---

## Key Diagrams to Draw in Exam

1. **5C CPS Architecture** — Connection → Conversion → Cyber → Cognition → Configuration (with brief description of each layer)
2. **CPS Feedback Loop** — Physical process → Sensors → Computation → Actuators → back to physical
3. **Smart Factory CPS Architecture** — sensors, edge nodes, cloud, AI layer, actuation (from file 01)
4. **Sensor Data Fusion Levels** — three-level pyramid: raw data → feature level → decision level
5. **AR Maintenance Workflow** — work order → scan asset → AR overlay → technician action → confirmation → update CMMS
6. **AI + Big Data Closed Loop** — Big Data layer → AI analytics layer → CPS action layer → feedback loop
7. **PLM Digital Thread** — Design (PLM) → Manufacturing (MES/ERP) → Field (CPS/IIoT) → back to PLM

---

## Quick-Revision Cheat Sheet

### CPS 5C Architecture
1. **Connection** — sensor acquisition and network
2. **Conversion** — raw data → meaningful information
3. **Cyber** — data processing, analytics, digital twin
4. **Cognition** — insight generation, decision support
5. **Configuration** — action feedback to physical world

### Big Data 5 Vs
| V | Meaning |
|---|---|
| Volume | Massive quantity |
| Velocity | High-speed generation |
| Variety | Multiple formats |
| Veracity | Data quality/trustworthiness |
| Value | Actionable insights |

### AR vs VR Summary
| | AR | VR |
|---|---|---|
| Real world | Enhanced by overlays | Replaced by virtual world |
| Hardware | Smart glasses, tablet | Headset (HMD) |
| Best for | Live maintenance, remote expert | Training, simulation |
| Internet needed | Yes (live data) | Optional |

### 5 AI Techniques
1. Supervised learning — classification/regression (labeled data)
2. Unsupervised learning — clustering/anomaly detection (no labels)
3. Reinforcement learning — adaptive control (trial and error)
4. Computer vision — visual inspection (CNN)
5. NLP — maintenance records analysis (unstructured text)

### PLM 4 Lifecycle Stages
1. Conception (requirements, business case)
2. Design/Development (CAD, simulation, testing)
3. Manufacturing (production, BOM, quality)
4. Service/EOL (maintenance, upgrades, decommissioning)

### Sensor Fusion Techniques
- **Kalman filter** — optimal estimate from noisy measurements
- **Bayesian fusion** — probabilistic combination of sensor beliefs
- **Dempster-Shafer** — handles uncertainty from multiple sources
- **ML-based fusion** — neural network learns best combination automatically

---

## Suggested Study Order

1. Start with `01-cyber-physical-systems.md` — this is the foundation of the whole unit
2. Then `02-next-generation-sensors.md` — CPS depends on sensors
3. Then `03-ar-and-vr-in-industry.md` — practical CPS application (highest exam frequency)
4. Then `04-ai-bigdata-advanced-analytics.md` — intelligence layer on top of CPS
5. Finish with `05-plm-and-collaborative-platforms.md` — lifecycle management across all the above

Practice: For any question asking you to "design" or "propose" a system, sketch the ASCII architecture from the relevant notes file first, then build your answer around it.
