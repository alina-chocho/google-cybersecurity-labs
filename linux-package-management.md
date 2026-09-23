# Linux Package Management: Managing Software via APT

## Project Overview
This project demonstrates foundational Linux system administration skills by managing software packages on a Debian-based distribution. The objective was to update package lists, install specific network utilities (nload and tcpdump), verify installations, and safely purge packages using the Advanced Package Tool (APT) package manager.

## Environment & Tools
- Operating System: Linux (Debian/Ubuntu-based distribution)
- Interface: Bash Terminal / Google Skills Environment
- Package Manager: APT (Advanced Package Tool)

## Technical Execution & Command Log
Below is the verified history log of the command sequence executed to audit, install, and manage the system applications:

```bash
clear
apt
sudo apt install nload
nload -h
sudo apt remove nload
nload -h
sudo apt install tcpdump
aptlist --installed
apt list --installed
sudo apt install nload
apt list --installed
history
```

## Key Competencies Demonstrated
- Privilege Escalation: Correctly using sudo to execute administrative software installations.
- Dependency Resolution: Leveraging apt to automatically fetch and resolve package dependencies.
- System Auditing: Using apt list --installed to verify the state of system binaries and track changes.
