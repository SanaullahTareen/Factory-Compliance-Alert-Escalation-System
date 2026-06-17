# 🏭 Factory Compliance & Alert Escalation System

An end-to-end automated Edge AI surveillance, natural language regulation parsing, and compliance auditing pipeline designed to monitor manufacturing shop floors in real time. 

This system bridges real-time **Computer Vision (YOLOv8)**, **Natural Language Processing (Regulatory PDFs)**, and **Operational Workflow Escalation** to detect safety anomalies, dynamically evaluate danger tiers, trigger real-time alarm states, and maintain mutable log trails.

---

## 🧰 Technologies & Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Ultralytics](https://img.shields.io/badge/YOLOv8-006400?style=flat&logo=analytics&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

## 📂 Core Pipeline Modules

| Module | Component | Techniques & Frameworks | Description |
|---|---|---|---|
| **Module 1** | [Detection Engine](./factory_compliance_system.ipynb) | YOLOv8n, OpenCV, Bounding Box Spatial Anchors | Video ingestion engine analyzing frames to spot walkway breaches, forklift overloads, and equipment boundaries. |
| **Module 2** | [Severity Matrix](./factory_compliance_system.ipynb) | Regulatory Mapping Context, Decision Rules | Classifies raw detection events into four specific hazard tiers (LOW, MEDIUM, HIGH, CRITICAL). |
| **Module 3** | [Escalation Pipeline](./factory_compliance_system.ipynb) | Condition Routing, JSON Stream Serialization | Real-time trigger routing logic. Appends low risk to file logs; pushes high risk to visual cockpit alerts instantly. |
| **Module 4** | [Report Generation](./outputs/) | SQLite3 API, Tabular Audit Trail, JSONL Streams | Auto-writes immutable auditing records capturing UUIDs, timestamps, section links, and behavioral classes. |
| **Module 5** | [Operations Dashboard](./factory_compliance_system.ipynb) | `ipywidgets`, Render Pipelines, Pandas Filtering | Interactive supervisor console featuring live feed simulators, scrolling alert counters, and historical logs. |

---

## 📊 System Execution Architecture

```text
 factory-compliance-system/
 │
 ├── Compliance_Policy_Manual.pdf    # Dynamic regulation manual source asset
 ├── factory_compliance_system.ipynb  # Complete execution pipeline & user cockpit
 ├── dataset_instructions.txt        # Registration text for 10 GB+ video dataset assets
 ├── requirements.txt                # Unified dependencies manifest
 └── outputs/                        # Persistent analytical data warehouse
     ├── compliance.db               # Relational SQL transaction ledger
     ├── compliance_log.csv          # Structured human-readable spreadsheet log
     ├── compliance_log.jsonl         # Chronological immutable data streams
     └── alerts.jsonl                # Active high-priority incident triggers
