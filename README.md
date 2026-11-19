<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:050816,50:0B2545,100:00D4AA&height=190&section=header&text=Dhia%20Benothmen&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Automotive%20Cybersecurity%20%7C%20SOC%20%2F%20Blue%20Team&descAlignY=58&descSize=15" width="100%"/>

**Final-Year Telecommunications Engineering Student**
Securing connected vehicles. Detecting threats. Automating defense.

![Automotive Security](https://img.shields.io/badge/Automotive-Security-00D4AA?style=for-the-badge)
![SOC](https://img.shields.io/badge/SOC-Blue%20Team-0B2545?style=for-the-badge)
![Location](https://img.shields.io/badge/Tunisia-050816?style=for-the-badge)

</div>

```text
d0ok@github:~$ whoami
```

I work at the intersection of **automotive cybersecurity** and **security operations**. My projects are built to be reproducible: I implement the mechanism or the attack, test it, then document the limitations honestly.

- **Automotive security:** SecOC-style message authentication, CAN intrusion detection, secure OTA, TARA (ISO/SAE 21434 style), AUTOSAR-style software components
- **SOC / Blue Team:** Wazuh detection engineering, SOAR automation and threat-intel enrichment, MITRE ATT&CK coverage analysis, ML anomaly detection
- **Engineering:** C, Python, Linux, Docker, Terraform, Ansible, CI/CD

---

## Automotive Cybersecurity

| Project | What it does | Stack |
|---|---|---|
| [**secure-ecu-simulator**](https://github.com/d0ok/secure-ecu-simulator) | AUTOSAR-inspired secure ECU in C: HMAC-SHA-256 message authentication, freshness counters with replay protection, persistent counter across restarts. Unit tests, fuzzing under ASan/UBSan, live SocketCAN integration test, CI and a threat model. | C, SocketCAN, CAN FD, OpenSSL |
| [**can-ids**](https://github.com/d0ok/can-ids) | Unsupervised CAN intrusion detection on the HCRL Car-Hacking dataset. Hybrid ID-whitelist + Isolation Forest reaches F1 0.90–0.96 per attack type; an LSTM baseline is documented as a negative result. Includes a threat model and security report. | Python, scikit-learn, TensorFlow |
| [**secure-ota-pipeline**](https://github.com/d0ok/secure-ota-pipeline) | Secure vehicle OTA CI/CD demo: CycloneDX SBOM, Grype vulnerability gate, GPG signing in a protected environment, mock backend, simulated ECU client with anti-rollback and A/B slots, plus a UN R156 gap analysis. | GitHub Actions, GPG, Grype, Flask, Python |
| [**can-security-lab**](https://github.com/d0ok/can-security-lab) | Replay, injection and DoS attacks on a virtual CAN bus with a detector for each, and an ISO/SAE 21434-style TARA. Honest about simulation limits: the flood test showed monitoring tools losing frames. | Python, SocketCAN, can-utils |
| [**can-sniffer-analyzer**](https://github.com/d0ok/can-sniffer-analyzer) | Simulates 6 ECUs on a virtual CAN bus (`vcan0`), captures the traffic and produces per-ID statistics (rate, period, jitter, varying bytes) with frequency, timeline and jitter plots. The traffic baseline that can-security-lab builds on. | Python, SocketCAN, can-utils |
| [**autosar-intelligent-lighting**](https://github.com/d0ok/autosar-intelligent-lighting) | Intelligent lighting function as five AUTOSAR-style SWCs, validated MIL and SIL (generated C) against a Python golden model across 16 scenarios, with ROS 2 replay and a Unity 3D demo. | MATLAB/Simulink, Embedded Coder, Python, ROS 2, Unity |

---

## SOC & Blue Team

| Project | What it does | Stack |
|---|---|---|
| [**soc-coverage-analyzer**](https://github.com/d0ok/soc-coverage-analyzer) | Maps Wazuh rules and declared log sources to MITRE ATT&CK, classifies coverage and telemetry gaps deterministically, and exports ATT&CK Navigator layers and reports. An optional local LLM (Ollama) only drafts recommendations, and its output is validated and flagged for human review. | Python, Wazuh, MITRE ATT&CK, Pydantic, Ollama, Streamlit |
| [**soc-as-code**](https://github.com/d0ok/soc-as-code) | Lightweight SOC pipeline deployed as code: Wazuh detects, n8n enriches alerts in parallel with VirusTotal, AbuseIPDB and AlienVault OTX, scores them, and opens DFIR-IRIS cases automatically. Active Response blocks SSH brute force. Docker Compose and Ansible (with Vault) deployment, validated component by component. | Wazuh, n8n, DFIR-IRIS, Docker, Ansible |
| [**siem-mobile-kpi**](https://github.com/d0ok/siem-mobile-kpi) | Real-time 4G/5G KPI supervision (RSRP, RSRQ, RSCP, Ec/N0) with custom Wazuh rules and Isolation Forest anomaly detection, on 18k+ field measurements. | Wazuh, Elasticsearch, Kibana, Filebeat, Python, Docker Compose |

## DevSecOps

| Project | What it does | Stack |
|---|---|---|
| [**vpn-devsecops**](https://github.com/d0ok/vpn-devsecops) | DevSecOps pipeline for an IPSec / TLS VPN: Terraform and Ansible deployment, Checkov and OPA policy gates, and automated attack tests (IKE brute force, downgrade, DoS) with ACL validation. | Terraform, Ansible, strongSwan, OpenVPN, Checkov, OPA, Scapy, GitHub Actions |

---

## Tech Stack

![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)
![Wazuh](https://img.shields.io/badge/Wazuh-005571?style=flat-square&logo=wazuh&logoColor=white)
![Elastic](https://img.shields.io/badge/Elastic-005571?style=flat-square&logo=elastic&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![ROS 2](https://img.shields.io/badge/ROS%202-22314E?style=flat-square&logo=ros&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)

**Automotive:** CAN / CAN FD · SocketCAN · SecOC concepts · UN R156 · ISO/SAE 21434 (TARA) · AUTOSAR-style SWCs · Simulink MIL/SIL
**SOC:** Wazuh · ELK · n8n (SOAR) · DFIR-IRIS · VirusTotal / AbuseIPDB / OTX enrichment · MITRE ATT&CK · detection engineering · Isolation Forest

**Supply chain:** CycloneDX SBOM · Grype · GPG signing · anti-rollback
**DevSecOps:** Terraform · Ansible · Checkov · OPA · strongSwan · GitHub Actions

---

## Next up

- AUTOSAR Classic mapping and ARXML generation for the lighting project
- Counter resynchronization and key rotation for the secure ECU simulator
- Live ROS 2 link between the lighting results and the Unity viewer

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dhiabenothmen/)

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=d0ok&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=d0ok&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117" />

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00D4AA,50:0B2545,100:050816&height=100&section=footer" width="100%"/>

</div>
