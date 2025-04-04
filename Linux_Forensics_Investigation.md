# ■ Linux Forensics Investigation - File Analysis

## ■ Objective
The objective of this investigation is to identify specific files based on various criteria such as ownership, content, permissions, and file metadata. This type of investigation is common in penetration testing and forensic analysis where understanding file attributes can reveal critical information about system vulnerabilities or suspicious activity.

## ■ Tools & Techniques Used
- **Command-Line Tools**: `find`, `grep`, `sha1sum`, `wc`
- **Linux Forensics**: File ownership, permission, and content analysis
- **Pattern Matching & Hash Verification**: Using regex and hash comparison to locate specific files

## ■ Key Findings / Evidence

| Action / Indicator                                    | Description                                                                                       |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Files owned by `best-group`                          | `find / -group best-group 2>/dev/null`                                                          |
| Files containing an IP address                      | `grep -Eorh "([0-9]{1,3}\.){3}[0-9]{1,3}" / -name "oiMO" 2>/dev/null`                         |
| File with SHA1 hash `9d54da7584015647ba052173b84d45e8007eba94` | `sha1sum /path/to/file`                                                                            |
| File containing 230 lines                           | `wc -l /path/to/file`                                                                            |
| Files owned by user ID `502`                       | `find / -user 502 2>/dev/null`                                                                  |
| Files executable by everyone                      | `find / -perm /111 2>/dev/null`                                                                |

## ■ Analysis Summary
- The investigation used Linux command-line tools to locate files based on various criteria:
  - Group ownership identification.
  - Regex-based IP address search.
  - File hashing for validation against known hashes.
  - Line count check for a file with exactly 230 lines.
  - Checking file ownership by a specific user ID.
  - Identifying files with global execute permissions.
- This approach mimics real-world forensic analysis and auditing tasks in a Linux environment.

## ■ Skills Demonstrated
- Regex-based pattern matching to locate IP addresses within files.
- Hash comparison using `sha1sum` for file integrity verification.
- Permission auditing using `find` with `-perm` flag.
- Ownership-based file identification using `-user` and `-group`.
- Forensic analysis of file attributes using Linux CLI tools.

## ■ Real-World Application
These skills are critical in penetration testing and digital forensics. Finding files based on ownership, permissions, content, or metadata is essential for:
- Detecting unauthorized changes to sensitive files.
- Identifying files with dangerous permissions.
- Validating file integrity using hash comparison.
- Searching for sensitive data leakage (e.g., IP addresses or credentials).

## ■ Lessons Learned
- Leveraging `find` with specific flags (`-group`, `-user`, `-perm`) is powerful for locating files under certain conditions.
- Regex can be applied effectively to extract IP addresses or other patterns from files.
- Using `sha1sum` to verify file integrity against known hashes is a straightforward but essential technique in forensics.
- Understanding how file permissions work is vital for assessing system security.

## ■ Completion Status
Self-guided investigation using Linux CLI tools to conduct forensic analysis of file attributes.

