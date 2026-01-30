# DSPM for AIoT (Public Reference Architecture)

This repository presents a **vendor-neutral, public reference architecture** for applying
**Data Security Posture Management (DSPM)** principles to **AIoT pipelines** (edge → stream → cloud).

## What this demonstrates
- Continuous data discovery across AIoT telemetry
- Sensitivity classification and risk tagging
- Monitoring and governance via policy intent
- **Lifecycle-aware Destroy semantics (simulated)**

> This project intentionally avoids destructive operations and cloud delete APIs.
> Destroy is modeled through **audit logs, tombstones, and retention plans** only.

---

## Architecture
- 📄 **Architecture Overview (PDF):** `architecture/ARCHITECTURE.pdf`
- 🖼️ **Architecture Diagram (PNG):** `diagrams/dspm_aiot_architecture.png`

---

## Notebooks (execution evidence)
Run in order:
1. `notebooks/01_ingest_aiot.ipynb`
2. `notebooks/02_discover_classify.ipynb`
3. `notebooks/03_monitor_govern.ipynb`
4. `notebooks/04_destroy_simulated.ipynb`

All notebooks are **public-safe**: no credentials, no cloud delete APIs, no irreversible actions.

---

## Security Note
Destroy operations are **simulated by design** to reflect enterprise governance,
legal hold requirements, and public-repo safety.
