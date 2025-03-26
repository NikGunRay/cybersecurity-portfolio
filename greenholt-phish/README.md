# 🕵️ The Greenholt Phish

## 🧭 Objective
Investigate a suspicious email forwarded by a sales executive at Greenholt PLC. The message raised red flags due to an unusual greeting, unexpected financial attachment, and mismatched addresses. My goal was to verify its legitimacy and assess the threat.

## 🧪 Tools & Techniques Used
- **Thunderbird** – Open and inspect `.eml` file
- **VirusTotal** – Analyze attachment hash
- **MXToolbox** – Review SPF and DMARC records
- **Command Line** – `file`, `sha256sum` for hash and type validation

## 🔍 Key Findings
| Indicator                  | Value                                                                 |
|----------------------------|-----------------------------------------------------------------------|
| **Transfer Reference**     | 09674321                                                              |
| **From Name**              | Mr. James Jackson                                                    |
| **Email Address**          | info@mutawamarine.com                                                |
| **Reply-To Address**       | info.mutawamarine@mail.com                                           |
| **Originating IP**         | 192.119.71.157                                                       |
| **IP Owner**               | Hostwinds LLC                                                        |
| **SPF Record**             | `v=spf1 include:spf.protection.outlook.com -all`                     |
| **DMARC Record**           | `v=DMARC1; p=quarantine; fo=1`                                       |
| **Attachment Name**        | `SWT_#09674321____PDF__.CAB`                                        |
| **Attachment Hash (SHA256)** | `2e91c533615a9bb8929ac4bb76707b2444597ce063d84a4b33525e25074fff3f`   |
| **File Size**              | 400.26 KB                                                            |
| **Actual File Extension**  | `.rar` (disguised as `.cab`)                                        |

## 📖 Analysis Summary
- Display name, sending address, and reply-to address were inconsistent.
- The attachment was disguised with a misleading file name and extension.
- SPF and DMARC were configured, but spoofing risk remained due to mismatch.
- Originating IP traced back to a hosting provider, not a business network.
- The `.cab` file was actually a `.rar` archive — a known obfuscation method for malware delivery.

## 🧠 Skills Demonstrated
- Email header and metadata analysis
- File extension obfuscation detection
- Threat intelligence basics (IP/domain reputation)
- Safe malware triage and static inspection

## 🧰 Real-World Application
This investigation reflects real SOC tasks like verifying phishing reports, analyzing headers, checking SPF/DMARC, and handling potentially malicious files safely.

## 🎓 Lessons Learned
This exercise sharpened my ability to break down suspicious emails, validate identity infrastructure, and uncover common phishing techniques using free, accessible tools.

## ✅ Completion Status
Self-guided investigation, inspired by a real-world scenario.
