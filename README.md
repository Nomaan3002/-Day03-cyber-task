# -Day03-cyber-task
# Day 3 – Nessus vulnerability scan of localhost (127.0.0.1) 

## 🎯 Task Objective:
Perform a basic vulnerability scan on local PC (127.0.0.1) using Nmap and identify security risks.

## 🛠 Tool Used:
- Nmap 7.97 with NSE Scripts (`--script vuln`)

## 📍 Target:
- Localhost (127.0.0.1)

## 📊 Summary of Results:

| Port  | Service        | Finding                                |
|-------|----------------|-----------------------------------------|
| 135   | msrpc          | Open (Windows RPC)                      |
| 445   | microsoft-ds   | Open (SMB port – no vuln confirmed)     |
| 8000  | Splunkd HTTP   | ✅ Slowloris Attack (CVE-2007-6750)     |
| 8089  | Splunkd HTTPS  | ⚠️ Possible CSRF Vulnerability          |

## 📁 Files Included:
- `vuln-scan.txt` → Nmap scan output
- `vulnerability-notes.txt` → Summary & learning
- `screenshot1.png`, `screenshot2.png` → Scan result images (if any)

## 🧠 Key Learnings:
- Realized how open services can lead to DoS or injection flaws
- Learned to interpret Nmap script outputs
- Saw importance of CVEs and mitigation

