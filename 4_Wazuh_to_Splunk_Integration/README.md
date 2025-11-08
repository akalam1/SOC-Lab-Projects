# 🔗 Wazuh to Splunk Log Forwarding

## 👋 Overview
This project integrates Wazuh alerts with Splunk Enterprise via a custom Python forwarder using the HTTP Event Collector (HEC).

---

## 🟋️ Architecture
```
Wazuh Manager (192.168.1.226)
      │
      │ JSON Forwarder (Python)
      ▼
Splunk Enterprise (192.168.1.159)
```

---

## 🔧 Forwarder Script
`/usr/local/bin/wazuh_to_splunk.py`
```python
# Forwards Wazuh alerts to Splunk HEC
SPLUNK_HEC = "http://192.168.1.159:8088/services/collector/event"
TOKEN = "********"
```

---

## 🗃️ Screenshots

| Screenshot | Description |
|-------------|--------------|
| ![hec_settings](screenshots/splunk_hec_settings.png) | Splunk HEC configuration |
| ![curl_test](screenshots/hec_success.png) | curl test returning Success |
| ![splunk_live](screenshots/splunk_live_alerts.png) | Live Wazuh alerts visible in Splunk |

---

## 🎠 Results
✅ Wazuh alerts mirrored to Splunk in real-time  
✅ Verified connection via HEC  
✅ Created dashboards for SSH brute-force and Sysmon activity
