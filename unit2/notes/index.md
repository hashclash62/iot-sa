---
title: Unit 2 Notes Index
parent: Unit 2 — IIoT Architecture & Analytics
nav_order: 3
---

# Unit 2 Notes Index — IIoT Data Monitoring

---

## Notes Files Map

| File | Topic | QB Questions Covered |
|---|---|---|
| [01-iot-gateway.md](./01-iot-gateway.md) | IoT Gateway definition, functions, system design, sensor integration | Q1, Q5, Q8, Q13 |
| [02-edge-computing.md](./02-edge-computing.md) | Edge computing, edge device programming, latency, edge vs cloud comparison | Q2, Q6, Q9, Q14, Q18, Q21 |
| [03-cloud-computing-and-iiot-platforms.md](./03-cloud-computing-and-iiot-platforms.md) | Cloud computing, IIoT cloud architecture, scalability, cloud platforms | Q3, Q7, Q15, Q24 |
| [04-predictive-maintenance-and-data-analytics.md](./04-predictive-maintenance-and-data-analytics.md) | Predictive maintenance workflow, 5 analytics types, AI/ML in PdM, strategy | Q4, Q11, Q19, Q20, Q26, Q27 |
| [05-dashboards-fault-detection-and-security.md](./05-dashboards-fault-detection-and-security.md) | Data acquisition, dashboards, fault detection methods, use case, security | Q10, Q12, Q16, Q17, Q22, Q23, Q25, Q28 |

---

## Syllabus Coverage Checklist

- [x] Define IoT gateway
- [x] Functions of an IoT gateway in IIoT systems
- [x] IoT Gateway for connecting sensors to cloud (system design)
- [x] IoT Gateway for integrating multiple sensor types
- [x] Define edge computing
- [x] Edge computing for local data processing in IIoT
- [x] Edge systems for reducing latency in smart factories
- [x] Edge device programming in IIoT
- [x] Define cloud computing
- [x] Cloud-based IIoT architecture
- [x] Cloud platforms for scalable data monitoring
- [x] Importance of scalability in IIoT platforms
- [x] Define predictive maintenance
- [x] Workflow of predictive maintenance
- [x] Data analytics techniques in IIoT (5 types)
- [x] AI analytics role in predictive maintenance
- [x] Real-time data acquisition in manufacturing
- [x] Role of dashboards in IIoT monitoring
- [x] Real-time dashboard design for industrial operations
- [x] Compare edge computing and cloud computing
- [x] Latency issues in IIoT systems
- [x] Security concerns in IIoT data monitoring
- [x] IIoT monitoring use case
- [x] Real-time fault detection in industrial machines
- [x] Design IIoT-based real-time monitoring system (production line)
- [x] Predictive maintenance strategy using IIoT data
- [x] Challenges in implementing real-time IIoT dashboards

---

## Key Diagrams to Draw in Exam

1. **IoT Gateway Architecture**
   - Draw: Sensors (Modbus/OPC-UA/PROFINET) → IoT Gateway → Cloud (MQTT)
   - Label gateway functions inside the box

2. **Edge vs Cloud Architecture**
   - Draw: Machine → Edge Node (local decisions, buffer) → Cloud (analytics, dashboard)
   - Show what happens at each layer

3. **Cloud IIoT Architecture Stack**
   - Layers: IoT Hub → Message Bus → Stream Analytics → Time-Series DB → ML Engine → Dashboard

4. **Predictive Maintenance Workflow**
   - 7-step flow: Data Collection → Pre-processing → Baseline → Anomaly Detection → Alert → Maintenance → Feedback

5. **Analytics Maturity Pyramid**
   - 4 levels: Descriptive → Diagnostic → Predictive → Prescriptive
   - Label each with what question it answers

6. **Real-Time Dashboard Layout**
   - Sketch with: machine status lights, KPI cards, time-series chart, alert panel

7. **OT/IT Network Segmentation (Security)**
   - Draw: Internet → Firewall → IT Network → DMZ/Firewall → OT Network → Machines

---

## Quick-Revision Cheat Sheet

### IoT Gateway — 7 Functions
1. Protocol translation (Modbus/OPC-UA → MQTT)
2. Data aggregation (bundle many sensors into one payload)
3. Data filtering and pre-processing
4. Local decision making / edge logic
5. Security and device authentication
6. Offline buffering (store when cloud is down)
7. Device management (firmware updates, health monitoring)

### Edge vs Cloud — 6-Point Comparison

| | Edge | Cloud |
|---|---|---|
| Location | Near machine | Remote data center |
| Latency | < 5ms | 50–500ms |
| Bandwidth | Low usage | High usage |
| Offline | ✅ Works | ❌ Needs internet |
| Scalability | Limited | Unlimited |
| Best for | Real-time control | Deep analytics, ML training |

### 5 Analytics Types

| Type | Question | Example |
|---|---|---|
| Descriptive | What happened? | OEE report last month |
| Diagnostic | Why did it happen? | Root cause of downtime |
| Predictive | What will happen? | RUL = 8 days |
| Prescriptive | What should I do? | Replace bearing on Day 5 |
| Real-time | What's happening now? | Temp rising 2°C/min |

### Predictive Maintenance — 7-Step Workflow
1. Collect sensor data (vibration, temp, current)
2. Pre-process (clean, feature-extract)
3. Establish baseline (normal operating range)
4. Detect anomalies / predict failure
5. Alert maintenance engineer
6. Perform maintenance (planned downtime)
7. Feed actual condition back to ML model

### Security Threats + Solutions

| Threat | Solution |
|---|---|
| Unauthorized access | Device authentication + RBAC |
| Ransomware | Network segmentation + offline backups |
| Data interception | TLS/SSL encryption |
| Denial of Service | Traffic filtering at gateway |
| Insider threats | RBAC + audit logging |
| Standard: IEC 62443 for industrial cybersecurity |

### Cloud Service Models
- **IaaS** = rent servers → run your own software
- **PaaS** = use a platform → build your own IIoT app
- **SaaS** = use ready-made software → subscribe to a cloud CMMS

### Key IIoT Platform Tools
- AWS IoT Core / Azure IoT Hub → Device management + messaging
- InfluxDB / AWS Timestream → Time-series storage
- Grafana / Power BI → Dashboards
- Azure ML / SageMaker → ML models
- Siemens MindSphere → Industrial-specific platform
