# 🛠️ Security Tools & Notes

This folder contains notes on security tools I’ve personally used or explored during hands-on labs, TryHackMe modules, and investigations. It's a living document and reflects tools relevant to my cybersecurity journey — especially as I transition from sales into a technical role.

---

## 🧪 Recon & Scanning

### 🔹 Nmap
- **Purpose**: Port scanning, service enumeration, OS detection.
- **Common Command**: `nmap -sV -A <target>`

### 🔹 Netcat
- **Purpose**: Manual connections, banner grabbing, reverse shells.
- **Example**: `nc -v <host> <port>`

### 🔹 Whois
- **Purpose**: Domain/IP ownership lookups (used in phishing analysis).
- **Example**: `whois <domain>`

### 🔹 Dig
- **Purpose**: DNS record querying and troubleshooting.
- **Example**: `dig @1.1.1.1 <domain>`

---

## 🔐 Email Phishing Analysis

### 🔹 Thunderbird
- **Used to**: Open and analyze `.eml` files (used in The Greenholt Phish investigation).
- **Why**: Review headers, attachments, and body for phishing indicators.

### 🔹 VirusTotal
- **Purpose**: Check file hashes and URLs for known threats.

### 🔹 MXToolbox
- **Purpose**: Inspect SPF, DKIM, and DMARC records for phishing detection.

---

## 🪟 Windows Tools

### 🔹 MSConfig
- Troubleshooting startup issues and boot configurations.

### 🔹 Event Viewer
- Viewing logs (login attempts, alerts, system events).

### 🔹 Task Manager & Resource Monitor
- Monitor system performance and running processes.

---

## 🐧 Linux CLI Tools

### 🔹 top / htop
- Real-time process monitoring.

### 🔹 netstat / ss
- List network connections and open ports.

### 🔹 ip / ifconfig
- View or configure network interfaces.

---

## 🌐 Web & HTTP

### 🔹 Curl
- Make manual HTTP/HTTPS requests.

### 🔹 Browser Dev Tools
- Inspect HTTP requests, status codes, and headers.

---

## 🧠 Other Tools To Explore Later

- 🕷 **Burp Suite** – Web application testing.
- 🧪 **Wireshark** – Network packet analysis.
- 💾 **Autopsy** – Digital forensics.
- 🧰 **Sysinternals Suite** – Windows internals toolkit.
- 🧙 **CyberChef** – Data transformation & decoding.

---

> ⚡ This list will evolve as I gain deeper technical experience across red and blue team tools. Feel free to fork or reference.
