# 🛡️ AI-IDS-Blocker

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Groq](https://img.shields.io/badge/AI-Groq%20LLaMA-orange?style=for-the-badge)
![Streamlit](https://img.shields.io/badge/Dashboard-Streamlit-red?style=for-the-badge)
![Windows](https://img.shields.io/badge/Windows-Firewall-blue?style=for-the-badge&logo=windows)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

### Real-Time Threat Detection & Auto-Blocking System

</div>

---

## 📸 Dashboard Preview

<div align="center">

![Dashboard](screenshots/idsdashboard1.png)

</div>

---

## 🔥 What This Does

This tool monitors your network in **real-time**, uses **Groq AI (LLaMA 3.3)** to analyze suspicious traffic, and **automatically blocks malicious IPs** via Windows Firewall!

```
Live Network Traffic
       ↓
 Scapy Capture
       ↓
Attack Detection
       ↓
Groq AI Analysis
       ↓
Threat Score > 75?
       ↓
Auto Block IP (Windows Firewall)
       ↓
Real-Time Dashboard Alert
```

---

## ✨ Features

- 📡 **Live Packet Capture** — Real-time network monitoring
- 🤖 **AI Threat Analysis** — Groq LLaMA 3.3 analyzes each attack
- 🚨 **Auto Classification** — CRITICAL/HIGH/MEDIUM/LOW severity
- 🚫 **Auto IP Block** — Windows Firewall integration
- 🖥️ **SOC Dashboard** — Alien theme, live alerts, blocked IPs
- 🔍 **Attack Detection** — Port Scan, SYN Flood, Brute Force, DoS
- 📝 **Alert Logging** — All threats + blocks saved to log files
- 📊 **Threat Score** — 0-100 AI-powered scoring system

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| Scapy | Live packet capture |
| Groq API (LLaMA 3.3) | AI threat analysis |
| Streamlit | SOC Dashboard UI |
| Windows Firewall (netsh) | Auto IP blocking |
| Npcap | Windows packet driver |

---

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/vasanth18-bad/AI-IDS-Blocker.git
cd AI-IDS-Blocker
```

### 2. Install Dependencies
```bash
pip install scapy groq streamlit python-dotenv
```

### 3. Install Npcap (Windows Only)
👉 [npcap.com/#download](https://npcap.com/#download)

### 4. Add API Key
Create `.env` file:
```
GROQ_API_KEY=your_groq_api_key_here
```
Get FREE API key: [console.groq.com](https://console.groq.com)

### 5. Run Project (Admin Required!)
```bash
# Right click -> Run as Administrator
run.bat

# Or manually:
# Terminal 1
python capture/ids_capture.py

# Terminal 2
python -m streamlit run dashboard/ids_dashboard.py
```

### 6. Open Dashboard
```
http://localhost:8501
```

---

## 📁 Project Structure

```
AI-IDS-Blocker/
├── AI_engine/
│   ├── __init__.py
│   └── ids_analyzer.py      # Groq AI threat analysis
├── blocker/
│   ├── __init__.py
│   └── ip_blocker.py        # Windows Firewall auto block
├── capture/
│   └── ids_capture.py       # Live packet capture + detection
├── dashboard/
│   └── ids_dashboard.py     # Streamlit SOC dashboard
├── logs/
│   ├── ids.log              # All traffic logs
│   ├── alerts.log           # AI threat alerts
│   └── blocked_ips.log      # Blocked IP list
├── screenshots/             # Portfolio screenshots
├── run.bat                  # One-click launcher (Admin)
├── .env                     # API keys (not in GitHub)
└── README.md
```

---

## 🎯 Detected & Blocked Threats

| Attack Type | Port | Severity | Action |
|------------|------|---------|--------|
| SSH Brute Force | 22 | 🔴 HIGH | Auto Block |
| Telnet Attack | 23 | 🔴 HIGH | Auto Block |
| RDP Attack | 3389 | 🔴 HIGH | Auto Block |
| Metasploit | 4444 | 🔴 CRITICAL | Auto Block |
| MySQL Attack | 3306 | 🟡 MEDIUM | Alert |
| FTP Attack | 21 | 🟡 MEDIUM | Alert |
| SYN Flood | Any | 🔴 HIGH | Auto Block |
| DoS Attack | Any | 🔴 HIGH | Auto Block |

---

## 🤖 AI Analysis Output

```
THREAT_SCORE: 85
SEVERITY: HIGH
ATTACK_CATEGORY: Brute Force
ATTACK_NAME: SSH Brute Force Attack
EXPLANATION: Multiple rapid connection attempts detected
RECOMMENDATION: Block source IP immediately
CONFIDENCE: HIGH

[AUTO BLOCK] Score 85 >= 75 — Blocking 192.168.1.100!
[BLOCKED] 192.168.1.100 | SSH Brute Force | Score: 85/100
```

---

## ⚠️ Requirements

- Windows OS (for Firewall integration)
- **Run as Administrator** (required for auto-blocking)
- Npcap installed
- Python 3.x
- Free Groq API key

---

## ⚠️ Legal Notice

> This tool is for **educational purposes only**.
> Use only on networks you **own or have permission** to monitor.
> Unauthorized network monitoring is **illegal**.

---

## 👨‍💻 Author

<div align="center">

**V** | Cybersecurity Portfolio Project

[![GitHub](https://img.shields.io/badge/GitHub-vasanth18--bad-black?style=for-the-badge&logo=github)](https://github.com/vasanth18-bad)

*Built with 💚 and blocked packets* 😈

</div>
