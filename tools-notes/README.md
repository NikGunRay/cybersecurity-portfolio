# 🔧 Security Tools & Notes

This section contains practical notes and summaries from hands-on cybersecurity tools used across labs, challenges, and real-world scenarios.
# 🔧 Security Tools & Commands I’ve Used

## 🧪 Recon & Scanning

### Nmap
- **Used for**: Port scanning, service detection.
- **Command**: `nmap -sV -A <target>`

### Netcat
- **Used for**: Manual connections, banner grabbing, reverse shells.
- **Command**: `nc -v <host> <port>`

### Whois
- **Used for**: IP/domain ownership (used in phishing analysis).
- **Command**: `whois <domain>`

### Dig
- **Used for**: DNS queries, troubleshooting.
- **Command**: `dig @1.1.1.1 <domain>`

---

## 🔐 Email Phishing Analysis

### Thunderbird
- **Used to**: Open `.eml` attachments.
- **Why**: To investigate phishing attempts visually.

### VirusTotal
- **Used for**: Scanning file hashes and links.
- **Workflow**: Hash attachments and look them up.

### MXToolbox
- **Used to**: Check SPF, DMARC, MX records during phishing cases.

---

## 🪟 Windows Tools

### MSConfig
- System configuration and startup debugging.

### Event Viewer
- Investigate logon events and system behavior.

### Task Manager / Resource Monitor
- Live process and resource usage monitoring.

---

## 🧠 Linux Tools

### `top`, `htop`
- Live process monitoring.

### `netstat`, `ss`
- View open connections and ports.

### `ip`, `ifconfig`, `ip addr`
- View network settings.

---

## 🌐 Web & HTTP

### Curl
- Used to make manual HTTP requests and test endpoints.

### Dev Tools (Chrome/Firefox)
- Viewing HTTP headers, analyzing site behavior.

---

## 🧪 Other Tools to Explore Later

- Burp Suite (web testing)
- Wireshark (packet analysis)
- Sysinternals Suite (Windows endpoint)
- Autopsy (forensics)
- CyberChef (data transformation)
