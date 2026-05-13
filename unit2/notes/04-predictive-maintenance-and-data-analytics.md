# Chapter 4: Predictive Maintenance & Data Analytics

---

## 4.1 Analogy — Your Car's Health vs. a Factory Machine's Health

If your car makes a grinding noise when braking, you take it in before the brakes fail completely. But most factories have traditionally waited for machines to fail — then scrambled to fix them. **Predictive maintenance** is like giving every factory machine a continuous health checkup, and calling the mechanic before the grinding noise even starts.

---

## 4.2 What is Predictive Maintenance?

**Predictive maintenance (PdM)** is a proactive maintenance strategy that uses real-time sensor data and analytics to predict when a machine component is likely to fail, so maintenance can be performed at the optimal time — before failure, but not too early.

It stands in contrast to:

| Strategy | How it works | Problem |
|---|---|---|
| **Reactive (breakdown) maintenance** | Fix after it fails | Unplanned downtime, possible safety risk |
| **Scheduled (preventive) maintenance** | Fix at fixed intervals (e.g., monthly) | May maintain too early (waste) or too late (failure) |
| **Predictive maintenance** | Fix when data shows wear is approaching critical threshold | Optimal — minimizes downtime and cost |

---

## 4.3 Workflow of Predictive Maintenance (Q20)

```
STEP 1: DATA COLLECTION
─────────────────────────────────────────────────────────
[Machine] → Sensors (vibration, temperature, current, pressure, acoustic)
         → IIoT Gateway → Cloud / Edge

STEP 2: DATA PRE-PROCESSING
─────────────────────────────────────────────────────────
Clean raw sensor data:
- Remove outliers (sensor glitches)
- Resample to consistent time intervals
- Engineer features (RMS vibration, peak frequency, kurtosis)

STEP 3: BASELINE ESTABLISHMENT
─────────────────────────────────────────────────────────
Collect 3–6 months of data on healthy machines
Define "normal operating range" for each sensor parameter

STEP 4: ANOMALY DETECTION / FAILURE PREDICTION
─────────────────────────────────────────────────────────
Compare real-time readings against baseline
Methods:
  - Threshold rules: "if vibration_rms > 3.0g → warning"
  - Statistical process control: detect drift from mean
  - ML model: predict Remaining Useful Life (RUL) in days

STEP 5: ALERT & RECOMMENDATION
─────────────────────────────────────────────────────────
- Alert sent to maintenance engineer (mobile/dashboard)
- Recommended action: "Replace bearing on Pump #12 within 7 days"
- Severity level: Normal / Warning / Critical

STEP 6: MAINTENANCE ACTION
─────────────────────────────────────────────────────────
Maintenance planned during next available window (low production)
Work order auto-created in CMMS
Required spare part ordered automatically

STEP 7: FEEDBACK & MODEL IMPROVEMENT
─────────────────────────────────────────────────────────
After maintenance: record actual condition of replaced component
Feed this ground truth back to ML model → model improves over time
```

---

## 4.4 Data Analytics Techniques Used in IIoT (Q19)

### 1. Descriptive Analytics — "What happened?"
Aggregates historical data to show what has occurred.
- **Example:** "Machine #5 was down for 14 hours last month. Bearing failures caused 60% of downtime."
- Tools: dashboards, reports, OEE calculations

### 2. Diagnostic Analytics — "Why did it happen?"
Drills into data to identify root cause.
- **Example:** "Bearing failures correlated with vibration exceeding 2.5g at 120Hz for more than 30 minutes."
- Tools: correlation analysis, Pareto charts, fishbone diagrams applied to data

### 3. Predictive Analytics — "What will happen?"
Uses statistical models and ML to forecast future events.
- **Example:** "Based on current vibration trend, this bearing will fail within 8 days."
- Tools: regression, ARIMA (time-series forecasting), LSTM neural networks, Random Forest

### 4. Prescriptive Analytics — "What should we do?"
Goes beyond prediction to recommend the optimal action.
- **Example:** "Replace bearing on Day 5 — this minimizes production loss while avoiding failure."
- Tools: optimization algorithms, digital twins, decision trees

### 5. Real-Time (Streaming) Analytics — "What is happening right now?"
Processes data as it arrives — continuous, in-flight analysis.
- **Example:** "Current temperature is rising at 2°C/minute — fan should be activated in 10 minutes."
- Tools: Apache Kafka, Apache Flink, Azure Stream Analytics

---

## 4.5 Analytics Techniques Summary

```
DATA MATURITY PYRAMID:

        ┌────────────────────────────────┐
        │ PRESCRIPTIVE: What to do?      │  ← Highest value
        │ (Optimization, recommendations) │
        ├────────────────────────────────┤
        │ PREDICTIVE: What will happen?  │
        │ (ML models, RUL forecasting)   │
        ├────────────────────────────────┤
        │ DIAGNOSTIC: Why did it happen? │
        │ (Root cause, correlation)       │
        ├────────────────────────────────┤
        │ DESCRIPTIVE: What happened?    │  ← Most common starting point
        │ (Reports, dashboards, KPIs)    │
        └────────────────────────────────┘
```

---

## 4.6 AI Analytics in Predictive Maintenance (Q27)

AI/ML dramatically improves predictive maintenance accuracy compared to simple threshold rules.

**Why threshold rules alone are limited:**
- A vibration reading of 2.6g might be fine at 40°C motor temperature, but dangerous at 80°C
- Simple thresholds can't capture these interactions between multiple variables
- They generate too many false alarms (alert fatigue) or miss real failures

**How ML improves this:**
- **Multi-variate analysis:** ML considers vibration + temperature + current + age simultaneously
- **Pattern recognition:** Learns specific failure signatures from historical failure data
- **Remaining Useful Life (RUL) prediction:** Instead of just "is it bad?" → "how many days until failure?"
- **Anomaly detection:** Unsupervised ML identifies unusual patterns even if we've never seen that specific failure before

**Common ML techniques for PdM:**
| Technique | Use Case |
|---|---|
| **LSTM (Long Short-Term Memory)** | Sequential time-series prediction of RUL |
| **Random Forest / Gradient Boosting** | Classification (Normal/Warning/Failure) |
| **Isolation Forest / Autoencoder** | Unsupervised anomaly detection |
| **ARIMA / Prophet** | Time-series trend forecasting |
| **SVM (Support Vector Machine)** | Fault type classification |

---

## 4.7 Developing a Predictive Maintenance Strategy (Q26)

A complete strategy has technical, organizational, and data components:

**Technical:**
- Select sensors based on known failure modes per machine type
- Deploy IIoT gateway with reliable connectivity and edge buffering
- Choose cloud platform with time-series storage and ML pipeline
- Train models on historical data; define alert thresholds and RUL targets

**Data:**
- Ensure sensor data quality (calibrate sensors, handle missing values)
- Collect failure history to provide labeled training data for ML
- Define a data retention policy (keep high-frequency data for 6 months, downsampled for 5 years)

**Organizational:**
- Integrate with CMMS for automatic work order creation
- Define maintenance engineer response workflow (alert → confirm → schedule → execute → document)
- Track KPIs: Mean Time Between Failures (MTBF), Mean Time To Repair (MTTR), Planned vs Unplanned maintenance ratio

---

## Quick Summary

- Predictive maintenance shifts maintenance from time-based to condition-based — using sensor data to predict failure before it happens
- Workflow: Collect data → Pre-process → Establish baseline → Detect anomalies → Alert → Maintain → Feedback
- 5 analytics types: Descriptive, Diagnostic, Predictive, Prescriptive, Real-Time
- AI/ML enables multi-variate analysis and Remaining Useful Life (RUL) prediction — far more powerful than simple threshold rules
- For a full PdM strategy: cover sensors + connectivity + cloud + ML + alerts + CMMS integration + organizational workflow
- Key KPIs: MTBF, MTTR, Planned vs Unplanned maintenance ratio
