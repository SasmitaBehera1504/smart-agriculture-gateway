# 🌱 Smart Agricultural Soil Moisture Gateway

A C++-based smart farming prototype that monitors soil moisture across multiple agricultural zones and determines whether irrigation is required.

## 📌 Project Description

The system represents a small agricultural setup with **three virtual soil-moisture probes**, each assigned to a different zone.

Every probe generates a moisture reading ranging from **0% to 100%**. The gateway analyzes these readings, identifies the current soil condition, and makes an automatic irrigation decision based on predefined moisture thresholds.

## 🌾 Sensor Setup

| **Probe** | **Agricultural Zone** | **Moisture Reading** |
|-----------|------------------------|----------------------|
| probe0 | Zone 1 | 25% |
| probe1 | Zone 2 | 55% |
| probe2 | Zone 3 | 80% |

## 💧 Soil Condition Rules

| **Moisture Range** | **Condition** | **Irrigation** |
|--------------------|---------------|----------------|
| 0–29% | DRY | ON |
| 30–70% | NORMAL | OFF |
| 71–100% | WET | OFF |

## 🔍 Sample Result

```text
Zone 1 → 25% → DRY    → Irrigation ON
Zone 2 → 55% → NORMAL → Irrigation OFF
Zone 3 → 80% → WET    → Irrigation OFF
```

## ⚙️ Processing Flow

```text
Virtual Moisture Probes
          ↓
     C++ Gateway
          ↓
   Read Moisture Data
          ↓
 Classify Soil Condition
          ↓
   DRY / NORMAL / WET
          ↓
Determine Irrigation Need
          ↓
      Pump ON / OFF
```

## 🎯 Objective

The primary objective is to demonstrate how a **multi-node sensor system** can collect environmental data and use simple decision logic to automate irrigation requirements for different agricultural zones.

## 🛠️ Technology Used

- **Language:** C++
- **Input:** Virtual soil-moisture sensor readings
- **Processing:** Moisture threshold-based classification
- **Output:** Irrigation pump status
- **Architecture:** Multi-node sensor gateway
