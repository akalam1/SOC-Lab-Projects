# 🎟️ Windows Sysmon Threat Analysis

## 📍 Overview
This project collects Windows Sysmon logs through Wazuh to analyze suspicious process and registry activity.

---

## 🧪 Setup
- **Windows Agent:** Sysmon + Wazuh Agent
- **Manager:** Wazuh Server (Ubuntu)
- **Event Source:** Microsoft-Windows-Sysmon/Operational

---

## ⚙️ Key Events
| Event ID | Description | MITRE ATT&CK |
|-----------|--------------|---------------|
| 1 | Process creation | T1059 – Command Execution |
| 3 | Network connection | T1049 – Network Discovery |
| 12 | Registry modification | T1112 – Modify Registry |
| 18 | Pipe connection | T1106 – Execution through API |

---

## 📾 Screenshots
| Screenshot | Description |
|-------------|--------------|
| ![sysmon_config](screenshots/sysmon_config.png) | Sysmon XML configuration |
| ![wazuh_sysmon](screenshots/wazuh_sysmon_alerts.png) | Sysmon alerts in Wazuh dashboard |
| ![attack_trace](screenshots/sysmon_process_tree.png) | Suspicious parent-child process chain |

---

## 🌟 Results
✅ Real-time Sysmon log ingestion  
✅ Mapped detections to MITRE ATT&CK  
✅ Visibility into Windows persistence mechanisms
