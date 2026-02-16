# TelemetryIQ 🚀  
AI-Powered Observability Intelligence Platform

TelemetryIQ is a hybrid machine learning system that transforms raw telemetry data into actionable operational intelligence.

Instead of just monitoring metrics, TelemetryIQ:
- Detects anomalies in real time
- Classifies incident root causes
- Evaluates cost efficiency using FinOps signals
- Provides explainable, structured outputs for dashboards and automation

---

## 🧠 Architecture Overview

TelemetryIQ uses a two-stage ML pipeline:

1️⃣ Anomaly Detection (Isolation Forest)  
Learns baseline system behavior and detects abnormal telemetry patterns.

2️⃣ Incident Classification (Random Forest)  
Classifies abnormal behavior into:
- Memory Leak
- Bad Deployment
- Traffic Spike
- Normal Variation

Additionally, FinOps metrics are computed to distinguish:
- Good scaling vs bad scaling
- Cost-effective vs inefficient spikes

---


---

## 📊 Example Output

```json
{
  "anomaly_score": 0.81,
  "is_anomaly": true,
  "incident_type": "MemoryLeak",
  "confidence": 0.87,
  "indicators": [
    "Elevated CPU usage",
    "Memory increasing trend"
  ],
  "features": {
    "mean_cpu": 90.0,
    "memory_trend": 2.7,
    "unit_economics_ratio": 0.46
  }
}
