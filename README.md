# WorkCheck Kachchh (PS000109) — Platform v3

[![SSIP Gujarat 2026](https://img.shields.io/badge/SSIP%20Gujarat-2026-blue?style=for-the-badge)](https://ssipgujarat.in/)
[![Live Platform](https://img.shields.io/badge/Live%20Platform-GitHub%20Pages-brightgreen?style=for-the-badge&logo=github)](https://jaypatel29042008-glitch.github.io/WorkCheck-Kachchh-Platform-v3/)
[![Backend](https://img.shields.io/badge/Backend-FastAPI%20%2B%20SQLite-teal?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> **Student Startup and Innovation Policy (SSIP Gujarat 2026) / Seva First Innovation Challenge (SFIC 2026)**  
> **Problem Statement PS000109:** Digital Occupational Health Monitoring & ABHA Health Locker for Industrial Workers (DDO Kachchh)

---

## 🌐 Live Website (Zero Install)
Open the platform directly in your browser:  
👉 **[https://jaypatel29042008-glitch.github.io/WorkCheck-Kachchh-Platform-v3/](https://jaypatel29042008-glitch.github.io/WorkCheck-Kachchh-Platform-v3/)**

*(Read-only client-side interactive preview with 128 workers, clinical triage, microclimate heat monitor, and legal exam compliance tracker).*

### 🔑 Demo Sign-In Accounts
| Role | Email | Password | What It Opens |
|---|---|---|---|
| **Clinic team** | `clinic@workcheck.demo` | `Demo-Clinic-2026` | Today's triage, all 128 worker health records, check recording, facility referrals |
| **District office** | `ddo@workcheck.demo` | `Demo-DDO-2026` | Macro taluka totals, heat & dust map, CSV exports (anonymous) |
| **Site supervisor** | `site@workcheck.demo` | `Demo-Site-2026` | Site monitor, heat index & WBGT, simulated Wokwi ESP32 IoT node |
| **Worker** | `worker@workcheck.demo` | `Demo-Worker-2026` | Worker health pass (Kishan P.), QR code, symptom reporting |

---

## 🚀 Key Features
- **Worker Health Triage**: Categorized tracking for 128 industrial workers across 5 Kachchh zones (Bhuj stone crushers, Abdasa cement plants, Mundra Port cargo, Kandla Port logistics, Little Rann salt pans).
- **Occupational Health Modules**:
  - Eyes & skin examinations
  - Audiometry / hearing impairment tracking
  - Blood pressure & cardiovascular health
  - Spirometry & lung health (silica dust exposure)
  - Hydration & kidney function monitoring
  - WBGT heat stress calculations
- **Compliance & Legal Exams**: Tracks Gujarat Factories Act 120-day annual mandatory health check compliance.
- **Hardware Integration**: ESP32 Wokwi IoT microclimate sensor node with real-time temperature, globe temp, and particulate matter telemetry.
- **ABHA Health Locker Architecture**: Designed for digital health record portability for migrant industrial workers.

---

## 💻 Run Full-Stack Locally (FastAPI + SQLite)
```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Start the server
python -m uvicorn app.main:app --port 8090
```
Then visit `http://localhost:8090` in your browser. On Windows, double-click `run.bat`.

---

## 📂 Repository Structure
```
├── index.html              # Static entrypoint for GitHub Pages
├── styles.css              # Classical high-contrast UI design system
├── icons.js                # SVG icon library
├── qrcode.js               # Client-side QR generation
├── js/                     # Modular frontend controllers
│   ├── boot.js             # Bootstrap & route handler
│   ├── charts.js           # SVG interactive data visualizations
│   ├── checkin.js          # Daily worker self check-in
│   ├── core.js             # State management & session store
│   ├── dashboard.js        # Supervisor tracking metrics
│   ├── facilities.js       # Kachchh medical facilities map & directory
│   ├── heat.js             # Taluka heat & dust analysis
│   ├── login.js            # Auth & demo switcher
│   ├── me.js               # Worker pass & QR viewer
│   ├── onboard.js          # Workplace & site registration
│   ├── site.js             # Real-time microclimate replay
│   ├── team.js             # Invite code generator & team manager
│   ├── today.js            # Clinical triage & prioritized actions
│   ├── trackers.js         # Health examination trackers
│   ├── wokwi.js            # IoT sensor bridge interface
│   └── workers.js          # 128-worker master directory
├── app/                    # FastAPI backend application
│   ├── core.py             # Auth, sessions, RBAC
│   ├── main.py             # API endpoints & data models
│   ├── orgs.py             # Organisation & workplace management
│   ├── security.py         # CSP, headers, rate limiting
│   └── trackers.py         # Health check logging & verification
├── data/                   # Reference SQLite database & facility tables
├── tests/                  # Pytest test suite (26 comprehensive tests)
├── wokwi/                  # ESP32 hardware sketch & Wokwi bridge
└── requirements.txt        # Python backend dependencies
```

---

## 📜 Academic & Ethics Notice
*All individual worker profiles, names, and health metrics are synthetic test fixtures designed for system validation. Environmental parameters are derived from scientific models and regional monitoring standards.*

**Author:** Jay Patel ([@jaypatel29042008-glitch](https://github.com/jaypatel29042008-glitch))  
**College:** LDRP Institute of Technology and Research (LDRP-ITR), Gandhinagar | Gujarat Technological University (GTU)