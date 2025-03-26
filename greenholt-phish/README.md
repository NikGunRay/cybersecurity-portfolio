# The Greenholt Phish 🕵️‍♂️

## Overview
As a SOC Analyst, I investigated a suspicious email forwarded by a Sales Executive at Greenholt PLC. The sender used an unusual greeting and included an unexpected file attachment related to a financial transaction that was never discussed. The goal was to determine the legitimacy of the message and assess potential threats.

## Objectives
- Investigate email header fields
- Verify sender identity and reply address
- Analyze attachment hash and type
- Validate SPF and DMARC configurations
- Identify infrastructure behind the message

## Key Findings

| Indicator                         | Value                                                                 |
|----------------------------------|-----------------------------------------------------------------------|
| **Transfer Reference Number**    | 09674321                                                              |
| **From Name**                    | Mr. James Jackson                                                    |
| **Email Address**                | info@mutawamarine.com                                                |
| **Reply-To Address**             | info.mutawamarine@mail.com                                           |
| **Originating IP**              | 192.119.71.157                                                       |
| **IP Owner**                     | Hostwinds LLC                                                        |
| **SPF Record**                   | `v=spf1 include:spf.protection.outlook.com -all`                     |
| **DMARC Record**                 | `v=DMARC1; p=quarantine; fo=1`                                       |
| **Attachment Name**             | `SWT_#09674321____PDF__.CAB`                                        |
| **Attachment Hash (SHA256)**    | `2e91c533615a9bb8929ac4bb76707b2444597ce063d84a4b33525e25074fff3f`   |
| **File Size**                    | 400.26 KB                                                            |
| **Actual File Extension**        | `.rar`                                                               |

## Analysis Summary
- The mismatch between the display name, email address, and reply-to address raised red flags.
- The attachment was disguised with a misleading file name and extension.
- SPF and DMARC records showed some protection, but potential spoofing risks remained.
- The originating IP was linked to Hostwinds LLC, not a reputable business network.
- The file's `.CAB` extension masked the true `.RAR` archive, commonly used to deliver malicious payloads.

## Tools Used
- **Thunderbird** – Open and inspect `.eml` file
- **VirusTotal** – Analyze hash of attachment
- **MXToolbox** – Review SPF/DMARC records
- **Command Line** – `file`, `sha256sum` for local hash and type validation

## Skills Demonstrated
- Email header and metadata analysis
- File extension obfuscation detection
- Threat intel basics (IP and domain reputation)
- Malware triage and safe handling
