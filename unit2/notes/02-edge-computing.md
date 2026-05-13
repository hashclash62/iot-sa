# Chapter 2: Edge Computing & Edge Systems

---

## 2.1 Analogy — The Local Doctor vs. the Specialist in the City

When you have a minor cut, you go to the local doctor next door — fast, immediate, and no need to travel. When you need complex surgery, you go to the specialist in the city who has all the equipment.

**Edge computing** is the local doctor — fast, local decisions made right where the data is generated. **Cloud computing** is the specialist — powerful analysis with all resources available, but with some travel time (latency).

In a factory, you need both: the edge for millisecond decisions, and the cloud for deep, long-term analysis.

---

## 2.2 What is Edge Computing?

**Edge computing** is a distributed computing model where data processing happens at or near the source of data generation — on the factory floor, on the machine, or in a nearby device — rather than being sent to a centralized cloud.

The "edge" refers to the boundary between the physical world and the digital network — the point where raw sensor data first enters the computational system.

---

## 2.3 Why Edge Computing in IIoT?

The core problem it solves is **latency + bandwidth + reliability**:

| Problem Without Edge | How Edge Solves It |
|---|---|
| Sending all sensor data to cloud = huge bandwidth cost | Edge filters/compresses data locally — only relevant data goes to cloud |
| Cloud round-trip = 50–500ms delay — too slow for safety systems | Edge processes locally in < 5ms |
| If internet goes down, factory goes blind | Edge keeps running and buffering even without cloud connectivity |
| Sending raw data exposes sensitive operational info | Edge can anonymize/aggregate before cloud transmission |

---

## 2.4 Edge System Architecture

```
   MACHINE / SENSOR
         |
         | (raw data, high frequency)
         v
   ┌─────────────────────┐
   │   EDGE DEVICE        │   <── Installed at/near machine
   │                      │
   │  - Local processing  │   → Runs threshold alerts
   │  - Anomaly detect    │   → Calculates running averages
   │  - Protocol convert  │   → Triggers local actuators
   │  - Data buffer       │   → Stores data if cloud down
   │  - Compression       │
   └──────────┬──────────┘
              │ (filtered, compressed, relevant data)
              │ MQTT / HTTPS
              v
       CLOUD PLATFORM
       (long-term storage, ML models, dashboards)
```

**Edge devices include:** Industrial PCs, Raspberry Pi, NVIDIA Jetson (for AI at edge), edge gateways (Moxa, Advantech), smart cameras.

---

## 2.5 Edge Device Programming in IIoT (Q14)

Edge devices run software that implements:

**1. Data Acquisition:**
Reading sensor values via Modbus, OPC-UA, or analog inputs. Done at high frequency (e.g., 100 readings/second).

**2. Local Processing Logic:**
- Threshold checking: `if vibration_rms > 2.5 mm/s: send_alert()`
- Statistical calculations: rolling averages, standard deviation
- Feature extraction: extract frequency components from vibration signal (FFT)

**3. ML Inference at Edge (TinyML):**
Pre-trained ML models (trained on cloud) deployed to edge. The edge device runs the model locally — e.g., classifying bearing condition as Normal/Warning/Critical based on vibration pattern — without cloud.

**4. Local Actuation:**
Based on local logic, edge can trigger outputs: turn on a relay, send a stop signal to a motor, flash a warning light.

**5. Data Forwarding:**
Send processed/filtered data to cloud via MQTT or REST API. Include metadata (device ID, timestamp, location).

**Programming languages used:** Python (MicroPython for constrained devices), C/C++ for real-time systems, Node-RED for flow-based edge logic.

---

## 2.6 Edge Computing Reducing Latency in Smart Factories (Q9)

**Scenario:** A robotic welding line needs to detect if a weld arc goes out of the acceptable voltage range and stop the robot within 10ms to prevent a defective weld.

**Without edge:**
```
Robot sensor → Cloud (network delay: 50ms) → Cloud detects issue → Cloud sends stop command → Robot stops
Total time: 100–200ms — robot has already made 5 more bad welds
```

**With edge:**
```
Robot sensor → Edge device (local detection: 2ms) → Edge sends stop signal to robot
Total time: < 10ms — weld stopped immediately
```

This is the core value of edge computing in safety-critical and quality-critical IIoT applications.

---

## 2.7 Edge Computing vs Cloud Computing — Full Comparison (Q18)

| Parameter | Edge Computing | Cloud Computing |
|---|---|---|
| **Processing location** | On/near the device (factory floor) | Remote data center |
| **Latency** | < 5ms (near real-time) | 50–500ms |
| **Bandwidth usage** | Low (pre-filtered data sent) | High (all raw data sent) |
| **Scalability** | Limited (per-device resources) | Virtually unlimited |
| **Offline capability** | Works without internet | Requires connectivity |
| **Cost per device** | Higher (local hardware) | Lower (pay-per-use cloud) |
| **Data privacy** | Higher (data stays local) | Lower (data leaves facility) |
| **Compute power** | Limited (embedded systems) | Very high (GPU clusters, TPUs) |
| **Best for** | Real-time control, safety, local anomalies | Long-term analytics, ML training, multi-site dashboards |
| **Example use** | Stop a machine when vibration spikes | Train a 6-month predictive maintenance model |

**Conclusion:** Edge and cloud are **complementary, not competing**. Best IIoT systems use both — edge for real-time, cloud for intelligence.

---

## 2.8 Latency Issues in IIoT Systems (Q21)

**What is latency?**
Latency is the time delay between an event happening in the physical world and the IIoT system responding to it.

**Sources of latency in IIoT:**

| Source | Typical Delay | Cause |
|---|---|---|
| Network transmission | 1–100ms | Distance, congestion, protocol overhead |
| Cloud processing | 10–500ms | Server load, database query time |
| Data aggregation at gateway | 1–50ms | Buffering interval |
| Communication protocol overhead | 1–20ms | Handshaking, encryption |

**Why latency matters:**
- A safety interlock that takes 500ms to respond is useless — the machine may have already injured a worker
- A quality control system that takes 2 seconds to detect a defect lets 20 defective parts through

**Solutions to latency:**
1. **Edge computing** — process at source, eliminate cloud round-trip
2. **Time-Sensitive Networking (TSN)** — industrial Ethernet standard that guarantees deterministic latency
3. **5G private networks** — low-latency wireless for mobile robots and AGVs
4. **Pre-processing on gateway** — reduce data volume before cloud transmission

---

## Quick Summary

- Edge computing = processing data at or near the machine, not in the cloud
- Solves three problems: latency (local speed), bandwidth (less data to send), resilience (works offline)
- Edge devices run data acquisition, threshold checks, ML inference, local actuation, and data forwarding
- Edge and cloud are complementary — edge for fast reactions, cloud for deep analysis
- Key comparison: edge = fast/local/limited; cloud = slow/remote/unlimited
- Latency is a critical IIoT challenge: edge computing and TSN are the primary solutions
