# 🛠️ Security Tools & Notes

## 🧭 Objective
Track the cybersecurity tools I’ve used or explored during labs, TryHackMe rooms, and real investigations. This living document reflects my technical transition from sales into cybersecurity and grows with my hands-on experience.

## 🧪 Tools & Techniques Used

### 🧪 Recon & Scanning
| Tool     | Purpose                                          | Example                                 |
|----------|--------------------------------------------------|-----------------------------------------|
| Nmap     | Port scanning, OS detection, service enum        | `nmap -sV -A <target>`                  |
| Netcat   | Manual connections, banner grabbing              | `nc -v <host> <port>`                   |
| Whois    | Domain/IP ownership info                         | `whois <domain>`                        |
| Dig      | DNS record queries                               | `dig @1.1.1.1 <domain>`                 |

### ✉️ Email Phishing Analysis
| Tool        | Use Case                                      |
|-------------|-----------------------------------------------|
| Thunderbird | View and analyze `.eml` files (headers, etc.) |
| VirusTotal  | Analyze hashes, URLs                          |
| MXToolbox   | Inspect SPF, DKIM, and DMARC configs          |

### 🪟 Windows Utilities
- **MSConfig** – Boot config and troubleshooting
- **Event Viewer** – View logs (logins, alerts)
- **Task Manager / Resource Monitor** – Analyze performance and processes

### 🐧 Linux CLI Tools
- `top` / `htop` – Live process monitoring
- `netstat` / `ss` – View open ports and connections
- `ip` / `ifconfig` – Check or configure network interfaces

### 🌐 Web & HTTP Tools
- `curl` – Manually craft HTTP(S) requests
- **Browser Dev Tools** – Inspect headers, requests, and status codes

## 📖 Analysis Summary
These tools cover a wide range of blue team use cases — from investigating phishing emails and inspecting logs to conducting scans and investigating systems. I’ve prioritized mastering foundational, CLI-based tools I can build on.

## 🧠 Skills Demonstrated
- Comfort with multi-platform tools (Windows/Linux/Web)
- DNS and email infrastructure analysis
- Manual investigation techniques (vs black-box scanning)
- Reconnaissance and enumeration workflows

## 🧰 Real-World Application
These are the tools defenders use every day — whether in a SOC, IR, or forensics role. Learning them by hand strengthens my ability to operate under pressure and pivot when automation fails.

## 🎓 Lessons Learned
I now understand that it’s not about knowing every tool — it’s about knowing how and when to use the right one. This collection reflects my growing confidence and tactical awareness.

## ✅ Completion Status
Ongoing — living document, updated as I learn.
