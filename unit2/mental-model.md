---
title: Unit 2 — IIoT Architecture & Analytics
nav_order: 3
has_children: true
---

# Unit 2 — Mental Model: IIoT Data Monitoring

---

## Topic Groups

### Group 1: IoT Gateway
**Core idea:** The IoT gateway is the bridge between the field (sensors, machines) and the digital world (cloud, analytics). It translates industrial protocols, aggregates data, and manages device connectivity.

Covers: Q1, Q5, Q8, Q13

---

### Group 2: Edge Computing & Edge Systems
**Core idea:** Edge computing moves data processing closer to where it's generated — on or near the machine — instead of sending everything to the cloud. This reduces latency and enables real-time local decisions.

Covers: Q2, Q6, Q9, Q14, Q18, Q21

---

### Group 3: Cloud Computing & IIoT Platforms
**Core idea:** Cloud platforms provide the scalable storage, compute, and analytics infrastructure to handle data from thousands of industrial devices across multiple sites.

Covers: Q3, Q7, Q15, Q24

---

### Group 4: Predictive Maintenance & Data Analytics
**Core idea:** IIoT generates rich time-series data from machines. Statistical and ML-based analytics applied to this data enable shift from reactive/scheduled maintenance to predictive, condition-based maintenance.

Covers: Q4, Q11, Q19, Q20, Q26, Q27

---

### Group 5: Real-Time Dashboards, Fault Detection & Monitoring
**Core idea:** Real-time dashboards visualize IIoT data for operators and managers. Fault detection algorithms identify machine problems as they happen — enabling immediate corrective action.

Covers: Q10, Q12, Q16, Q17, Q23, Q25, Q28

---

### Group 6: Security, Scalability & Challenges in IIoT
**Core idea:** Connecting industrial systems to digital networks introduces cybersecurity risks. Scaling IIoT platforms from one plant to hundreds requires architectural planning.

Covers: Q22, Q24, Q28

---

## Topic Dependency Map

```
Sensors / Machines (Physical World)
          |
   [IoT Gateway]         <-- Group 1
   (protocol translation, aggregation)
     /         \
    /           \
[Edge          [Cloud Platform]    <-- Groups 2 & 3
Computing]      (scalable storage
(local,          + analytics)
 fast)               |
    \           [Data Analytics]   <-- Group 4
     \          (predictive maint.,
      \          AI/ML models)
       \              |
        [Real-Time Dashboard]      <-- Group 5
        (monitoring, fault detect)
              |
     [Security & Scalability]      <-- Group 6
     (protecting & growing the system)
```

---

## High-Frequency Topics Table

| Topic | Questions | Frequency |
|---|---|---|
| IoT Gateway functions & design | Q1, Q5, Q8, Q13 | ⭐⭐⭐⭐ |
| Edge computing vs Cloud computing | Q2, Q6, Q9, Q14, Q18 | ⭐⭐⭐⭐⭐ |
| Predictive maintenance workflow | Q4, Q11, Q20, Q26 | ⭐⭐⭐⭐ |
| Real-time dashboards | Q10, Q17, Q25, Q28 | ⭐⭐⭐⭐ |
| Cloud platforms for IIoT | Q3, Q7, Q15, Q24 | ⭐⭐⭐ |
| Data analytics techniques | Q11, Q19, Q27 | ⭐⭐⭐ |
| Fault detection | Q12, Q23 | ⭐⭐ |
| Security concerns | Q22 | ⭐⭐ |
| Scalability | Q24 | ⭐⭐ |
| Latency issues | Q21 | ⭐⭐ |

---

## Must Master vs Good to Know

| Must Master | Good to Know |
|---|---|
| IoT gateway definition, functions, and system design | Specific gateway vendors (Siemens, Moxa) |
| Edge vs Cloud computing — structured comparison | Edge computing hardware specs |
| Predictive maintenance concept and workflow (full diagram) | Specific ML algorithms (LSTM, random forest) |
| Cloud IIoT architecture (devices → gateway → cloud) | Specific platforms (AWS IoT, Azure IoT Hub) |
| Real-time dashboard purpose, components, and design | Dashboard tool specifics (Grafana, Tableau) |
| Data analytics techniques (5 key types) | Deep mathematics of each technique |
| Latency issue explanation + edge computing as solution | Network QoS configurations |
| Security concerns + mitigations (3–4 points) | Full IEC 62443 standard details |
