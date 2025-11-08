# 👀 Wazuh SIEM Lab – Threat Detection & Log Correlation

## 📌 Overview
This lab demonstrates a complete **Wazuh SIEM deployment** for detecting, monitoring, and analyzing security events across multiple agents (Ubuntu, Kali, Windows).  
It forms the foundation of my SOC analyst portfolio.

---

## 🏡 Architecture
- **Manager/Dashboard:** Ubuntu Server (`192.168.x.x`)
- **Agents:** Ubuntu server, Kali Linux, Windows 10
- **Tools:** Wazuh, Filebeat, Elasticsearch, Kibana

```
Wazuh Manager → Filebeat → Wazuh Indexer → Wazuh Dashboard
        ↑
  Agents (Ubuntu/Kali/Windows)
```

---

## ⚙️ Key Configurations
- Installed Wazuh Manager, Indexer, and Dashboard
- Connected Linux and Windows agents
- Verified heartbeat & log flow in dashboard
- Enabled File Integrity Monitoring (FIM) module
- Configured Sysmon on Windows

---

## 📟 Screenshots

| Screenshot | Description |
|-------------|--------------|
| ![dashboard](screenshots/wazuh_dashboard.png) | Wazuh dashboard showing connected agents |
| ![filebeat](screenshots/filebeat_config.png) | Filebeat configuration for secure log forwarding |
| ![indexer](screenshots/indexer_status.png) | Wazuh Indexer healthy and receiving data |
| ![fim](screenshots/fim_alerts.png) | File Integrity Monitoring (FIM) alerts detected |

---

## 🔍 Example Commands
```bash
sudo systemctl status wazuh-manager
sudo tail -f /var/ossec/logs/ossec.log
sudo filebeat test output
```

---

## 🌟 Results
✅ Successful multi-agent SIEM setup  
✅ Real-time event visibility across Linux and Windows  
✅ Foundation for advanced detection use cases (Sysmon, Splunk, etc.)

---

## 🧑‍🔧 Author
**Abul Kalam**  
🎓 B.S. Computer Science | CompTIA Security+  
🔗 [LinkedIn](https://www.linkedin.com/in/abulkalam) | [GitHub](https://github.com/akalam1)
