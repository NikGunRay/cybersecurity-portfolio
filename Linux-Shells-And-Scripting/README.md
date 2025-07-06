# Linux Shells & Scripting (TryHackMe)

## Objective
Hands-on walkthrough of Linux shell interaction, shell types, and scripting fundamentals — including variables, loops, and conditionals. Final exercise involved editing and executing a Bash script to locate a hidden flag in system logs.

## Tools Used
- Bash
- `nano`, `chmod`, `grep`, `cat`, `sudo`
- Ubuntu CLI (via TryHackMe’s AttackBox)

## Key Skills Demonstrated
- Bash scripting and logic debugging
- File permissions and script execution
- Grep usage for pattern matching in log files
- Looping through files with wildcard expansion
- Root privilege usage and directory awareness

## Flag Location
The flag (`thm-flag01-script`) was found in `/var/log/authentication.log` after correcting the script’s logic.

## Lessons Learned
- Wildcards inside quotes don’t expand — they must be unquoted to work in loops.
- Quirky questions like “Where is the cat sleeping?” are often hidden in plaintext log files.
- Even provided scripts may contain intentional flaws to test debugging skills.

