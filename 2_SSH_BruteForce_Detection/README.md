# 🚨 SSH Brute-Force Attack Detection (Wazuh + Splunk)

## 📍 Overview
This project simulates and detects SSH brute-force attempts using Wazuh correlation rules and Splunk dashboards.

---

## 🧪 Lab Setup
- **Attacker:** Kali Linux (`hydra`)
- **Target:** Ubuntu Server (Wazuh Agent)
- **SIEM:** Wazuh Manager & Splunk

---

## 🔧 Attack Simulation
```bash
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://192.168.x.x -t 4
```

---

## 📾 Screenshots

| Screenshot | Description |
|-------------|--------------|
| ![hydra_attack](screenshots/hydra_attack.png) | Hydra brute-force running from Kali |
| ![alerts](screenshots/wazuh_bruteforce_alerts.png) | Wazuh alert detecting multiple failed SSH attempts |
| ![splunk_dashboard](screenshots/splunk_dashboard.png) | Splunk dashboard showing attacker IPs and trends |

---

## 📊 Splunk Search Example
```spl
index=wazuh ("Failed password" OR "authentication failure")
| stats count by srcip, user
| sort -count
```

---

## 🌟 Results
- Wazuh triggered SSH brute-force rule (MITRE ATT&CK T1110)  
- Splunk visualized top attacking IPs and targeted users  

---

## 🧑‍💻 Author
**Abul Kalam**
