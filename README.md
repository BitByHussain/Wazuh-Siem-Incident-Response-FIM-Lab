# Wazuh-Siem-Incident-Response-FIM-Lab
Automated Threat Detection, FIM, and Incident Response with Wazuh SIEM on virutal machine highlighting key findings and remadition steps

# Automated Threat Detection, FIM, and Incident Response with Wazuh SIEM

## Project Overview

This project involves setting up a Wazuh SIEM lab on virtual machines, deploying a centralized security manager and an endpoint monitoring agent. The goal of this project is to detect unauthorized system changes using File Integrity Monitoring, integrate VirusTotal to catch malicious files, and set up automated scripts to stop attacks immediately.

## Tools Used

* Wazuh SIEM Platform: Centralized security manager and endpoint agent used for log collection, monitoring, and alerting.
* VirusTotal API: Threat intelligence integration used to automatically cross-reference file hashes and scan for malware.
* VMware: The virtualization platform (hypervisor) used to host and run the lab environment virtual machines.
* Bash Shell: Used to create the custom script for automatic file removal on the Linux agent.
