# 📎 File Integrity Monitoring (FIM) with Wazuh

## 👋 Overview
Monitors and detects unauthorized file modifications in critical system directories using Wazuh’s FIM module.

---

## 🔧 Configuration
`/var/ossec/etc/ossec.conf`
```xml
<syscheck>
  <directories>/etc,/usr/bin,/home</directories>
  <ignore>/etc/mtab</ignore>
</syscheck>
```

---

## 🗃️ Screenshots
| Screenshot | Description |
|-------------|--------------|
| ![fim_alert](screenshots/fim_alert.png) | Wazuh FIM alert showing modified file |
| ![dashboard_fim](screenshots/fim_dashboard.png) | Dashboard view of recent integrity events |

---

## 🎠 Results
✅ Detected unauthorized file changes  
✅ Logged events mapped to MITRE ATT&CK T1070.004  
✅ Demonstrated host-level detection capabilities
