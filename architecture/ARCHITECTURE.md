# DSPM for AIoT — Architecture Overview 

This document describes a **public reference architecture** for applying **Data Security Posture Management (DSPM)** principles to **AIoT (AI + IoT)** data pipelines that span **edge devices, streaming layers, and cloud systems**.

The architecture is paired with an **execution-ready notebook flow** that demonstrates each DSPM phase using **synthetic data only**.

---

## Architecture Diagram

> Refer to `architecture/ARCHITECTURE.pdf` for the full visual reference.

The architecture models:
- Edge devices generating telemetry and sensor data
- Streaming and ingestion layers
- Cloud analytics, policy, and governance layers
- DSPM controls applied **across the full data lifecycle**

---

## DSPM Lifecycle Mapping

| DSPM Phase | Implementation in v3.2 |
|-----------|------------------------|
| **Discover** | Edge telemetry and streaming data discovery |
| **Classify** | Sensitivity and PII tagging; risk scoring |
| **Monitor** | Access signals (simulated) and drift indicators |
| **Protect** | Policy gates (intent) and control recommendations |
| **Govern** | Retention and lineage modeling using a YAML policy file |
| **Destroy** | **Simulation only**: audit logs, tombstones, deletion plans (no hard delete) |

> ⚠️ The **Destroy** phase is intentionally modeled as *governance intent*, not execution.

---

## Key Design Decisions

### 1. Public-safe by default
- No credentials
- No destructive calls
- No cloud-provider-specific delete APIs
- Synthetic datasets only

This ensures the repository is safe for **public GitHub sharing**.

---

### 2. Governance intent vs. execution
- Policies generate **deletion plans** and **tombstones**
- No irreversible delete operations are performed
- Models real-world enterprise approval and audit workflows

---

### 3. Interview-ready by design
- Notebooks produce **deterministic outputs**
- Clear audit logs and lifecycle transitions
- Emphasis on **explainability** over automation

This makes the architecture suitable for:
- Technical interviews
- Architecture walkthroughs
- Security and governance discussions

---

## What This Architecture Is (and Is Not)

**This is:**
- A DSPM reference architecture for AIoT systems
- A lifecycle-oriented security and governance model
- A notebook-driven, explainable implementation

**This is not:**
- A vendor product
- A deployable production system
- An automated data-destruction pipeline

---

## Intended Audience

- Security Architects
- AI / ML Platform Engineers
- Embedded & AIoT Engineers
- DevSecOps and Data Governance teams

---

## Version

**v3.2** — Public, notebook-driven reference architecture
