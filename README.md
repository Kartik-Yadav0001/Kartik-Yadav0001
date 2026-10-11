<div align="center">
  <img src="assets/cybersecurity-banner.png" alt="Kartik Yadav - Cybersecurity, SOC, Network Security" width="100%" />
</div>

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Kartik--Yadav0001-0B1626?style=flat-square&logo=github&logoColor=00FF88)](https://github.com/Kartik-Yadav0001)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kartikyadav07-0B1626?style=flat-square&logo=linkedin&logoColor=00D9FF)](https://www.linkedin.com/in/kartikyadav07/)

</div>

## `$ cat about.txt`

I'm a B.Tech Computer Science student at **Lovely Professional University** focused on defensive security: SOC operations, SIEM concepts, network traffic analysis, threat detection, and incident response. I learn by building, so most of my work here is hands-on projects that I document and keep improving.

**Objective:** a cybersecurity or SOC analyst internship where I can apply detection and network-analysis fundamentals, learn from working analysts, and contribute to real monitoring and investigation work.

I also enjoy Python development, automation, and algorithms, and I build full-stack projects alongside my security work.

## `$ cat focus-areas.txt`

- **Threat detection:** rule-based detections mapped to MITRE ATT&CK techniques
- **Network security:** packet capture, flow analysis, and protocol-level investigation
- **SOC and SIEM concepts:** alert triage, incident workflows, and log analysis
- **Digital forensics and incident response:** evidence-based investigation and documentation
- **Automation:** Python tooling for parsing, detection, and reporting

## `$ ls ~/tech-stack`

> Experience level varies by tool. "Used in projects" means I have used it in the repositories below. "Learning" means I am studying it and have not yet built something substantial with it. I have no professional work experience to claim yet.

**Used in projects**

| Area | Technologies |
| :-- | :-- |
| Security and networking | ![Wireshark/TShark](https://img.shields.io/badge/Wireshark%20%2F%20TShark-0B1626?style=flat-square&logo=wireshark&logoColor=00FF88) ![Scapy](https://img.shields.io/badge/Scapy-0B1626?style=flat-square&logoColor=00FF88) ![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK%20mapping-0B1626?style=flat-square&logoColor=00FF88) |
| Languages | ![Python](https://img.shields.io/badge/Python-0B1626?style=flat-square&logo=python&logoColor=00FF88) ![C++](https://img.shields.io/badge/C%2B%2B-0B1626?style=flat-square&logo=cplusplus&logoColor=00FF88) ![JavaScript](https://img.shields.io/badge/JavaScript-0B1626?style=flat-square&logo=javascript&logoColor=00FF88) ![TypeScript](https://img.shields.io/badge/TypeScript-0B1626?style=flat-square&logo=typescript&logoColor=00FF88) |
| Backend and data | ![FastAPI](https://img.shields.io/badge/FastAPI-0B1626?style=flat-square&logo=fastapi&logoColor=00FF88) ![Node.js](https://img.shields.io/badge/Node.js-0B1626?style=flat-square&logo=nodedotjs&logoColor=00FF88) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0B1626?style=flat-square&logo=postgresql&logoColor=00FF88) ![Redis](https://img.shields.io/badge/Redis-0B1626?style=flat-square&logo=redis&logoColor=00FF88) ![scikit-learn](https://img.shields.io/badge/scikit--learn-0B1626?style=flat-square&logo=scikitlearn&logoColor=00FF88) |
| Frontend and dashboards | ![React](https://img.shields.io/badge/React-0B1626?style=flat-square&logo=react&logoColor=00D9FF) ![Next.js](https://img.shields.io/badge/Next.js-0B1626?style=flat-square&logo=nextdotjs&logoColor=00D9FF) ![Streamlit](https://img.shields.io/badge/Streamlit-0B1626?style=flat-square&logo=streamlit&logoColor=00D9FF) |
| Platform and tooling | ![Docker](https://img.shields.io/badge/Docker%20Compose-0B1626?style=flat-square&logo=docker&logoColor=00D9FF) ![Prometheus](https://img.shields.io/badge/Prometheus-0B1626?style=flat-square&logo=prometheus&logoColor=00D9FF) ![Grafana](https://img.shields.io/badge/Grafana-0B1626?style=flat-square&logo=grafana&logoColor=00D9FF) ![Git](https://img.shields.io/badge/Git-0B1626?style=flat-square&logo=git&logoColor=00D9FF) ![Linux](https://img.shields.io/badge/Linux-0B1626?style=flat-square&logo=linux&logoColor=00D9FF) |

**Learning**

![Wazuh](https://img.shields.io/badge/Wazuh-0B1626?style=flat-square&logoColor=FFFFFF) ![SIEM workflows](https://img.shields.io/badge/SIEM%20workflows-0B1626?style=flat-square&logoColor=FFFFFF) ![Incident response](https://img.shields.io/badge/Incident%20response-0B1626?style=flat-square&logoColor=FFFFFF) ![Digital forensics](https://img.shields.io/badge/Digital%20forensics-0B1626?style=flat-square&logoColor=FFFFFF)

## `$ ls ~/projects`

### SentinelX: SOC and XDR Platform

*Flagship project, in active development.* A FastAPI-based platform for security operations: event ingestion, rule-based detection, alerting, and incident tracking.

- **Implemented so far:** Docker Compose stack (PostgreSQL, Redis, OpenSearch, Nginx, Prometheus, Grafana), a FastAPI service with a health endpoint, SQLAlchemy models for users, endpoints, security events, alerts, incidents, indicators, incident timelines, and audit logs, and a detection engine with 8 initial rules
- **Services:** alert, incident, and event services; JSON structured logging; environment-based configuration; role-based seed users
- **Planned:** Next.js frontend (listed in the repository as a later sprint)
- **Tech:** Python, FastAPI, SQLAlchemy, PostgreSQL, Redis, OpenSearch, Docker, Prometheus, Grafana
- **Repository:** [Kartik-Yadav0001/SOC-XDR](https://github.com/Kartik-Yadav0001/SOC-XDR)

### Network Traffic Analysis and Threat Detection

A Python pipeline that turns packet captures into flows, baselines normal behavior, and flags suspicious activity for an analyst to review.

- **Pipeline:** PCAP parsing (TShark with a Scapy fallback), bi-directional 5-tuple flow aggregation, and a behavioral baseline profile
- **Detections:** 8 modular rules covering port scanning, SYN flood, ARP poisoning, DNS anomalies and tunneling, periodic C2 beaconing, data exfiltration, cleartext email credentials, and TCP reset anomalies, with MITRE ATT&CK mapping where applicable
- **Output:** a 0-100 risk score with severity levels, plus a Streamlit analyst console with exportable incident reports
- **Quality:** pytest suite, architecture and detection docs, and investigation playbooks in the repository. Threat scenarios are synthetic or local loopback traffic, so results are a learning exercise, not a production benchmark
- **Tech:** Python, TShark/Wireshark, Scapy, Streamlit, Plotly, pytest
- **Repository:** [Kartik-Yadav0001/Network-Traffic-Analysis](https://github.com/Kartik-Yadav0001/Network-Traffic-Analysis)

### Metro Route Finder

A metro navigation system built around a graph engine, with a REST API and a React interface.

- **Algorithms in the C++17 engine:** Dijkstra, BFS, DFS, A\*, bidirectional search, Floyd-Warshall, and Yen's K-shortest paths
- **API:** Node.js and Express with JWT-protected admin routes, request size limits, rate limiting, and atomic file writes
- **Frontend:** React with an interactive Leaflet map, algorithm comparison charts, and graph analytics
- **Quality:** C++ unit tests, API integration tests, CI workflow, and MIT license
- **Tech:** C++17, CMake, Node.js, Express, React
- **Links:** [Repository](https://github.com/Kartik-Yadav0001/metro-route-finder) | [Live application](https://metro-route-finder-1.onrender.com/)

### AI Healthcare Assistant

A full-stack symptom-based disease prediction app. Built for learning; it is not a medical tool.

- **Backend:** FastAPI, SQLAlchemy, scikit-learn RandomForest classifier, JWT authentication, input validation, and rate limiting
- **Frontend:** React (Vite), Tailwind CSS, and Recharts dashboards
- **Tech:** Python, FastAPI, scikit-learn, React
- **Repository:** [Kartik-Yadav0001/AI-healthcare](https://github.com/Kartik-Yadav0001/AI-healthcare)

### Thread Weaver

An interactive thread-pool simulator that visualizes workload distribution, locking, and synchronization.

- **Tech:** Next.js, TypeScript, Tailwind CSS
- **Repository:** [Kartik-Yadav0001/Thread_management](https://github.com/Kartik-Yadav0001/Thread_management)

## `$ cat currently-learning.txt`

- SIEM workflows and security event triage
- Log analysis, alert investigation, and incident-response fundamentals
- Packet-level analysis and network protocols
- Linux administration and Python automation
- MITRE ATT&CK and detection engineering

## `$ github --stats`

<div align="center">

<a href="https://github.com/Kartik-Yadav0001">
  <img height="165" alt="GitHub stats card" src="https://github-readme-stats.vercel.app/api?username=Kartik-Yadav0001&show_icons=true&hide_border=true&bg_color=0B1626&title_color=00FF88&icon_color=00D9FF&text_color=E8F4FA" />
</a>
<a href="https://github.com/Kartik-Yadav0001?tab=repositories">
  <img height="165" alt="Most used languages card" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kartik-Yadav0001&layout=compact&hide_border=true&bg_color=0B1626&title_color=00FF88&text_color=E8F4FA" />
</a>

</div>

<sub>Cards are rendered by a third-party service and may occasionally be slow or unavailable. Language data only reflects public repositories. See the [GitHub profile](https://github.com/Kartik-Yadav0001) for live activity.</sub>

## `$ cat credentials.txt`

No certifications listed yet. I would rather leave this section honest than pad it. Verified certifications will be added here as I earn them.

<!-- Maintainer note: add each certification as "- Name, Issuer, Year, [credential link]" only once it is verified. -->

## `$ connect --with-me`

- **GitHub:** [Kartik-Yadav0001](https://github.com/Kartik-Yadav0001)
- **LinkedIn:** [kartikyadav07](https://www.linkedin.com/in/kartikyadav07/)

---

<div align="center">

**Investigate with evidence. Build defenses that can be explained. Document what I learn.**

</div>
