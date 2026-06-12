# Wazuh-Siem-Incident-Response-FIM-Lab
Automated Threat Detection, FIM, and Incident Response with Wazuh SIEM on virutal machine highlighting key findings and remadition steps

# Automated Threat Detection, FIM, and Incident Response with Wazuh SIEM

## Project Overview

This project involves setting up a Wazuh SIEM lab on virtual machines, deploying a centralized security manager and an endpoint monitoring agent. The goal of this project is to detect unauthorized system changes using File Integrity Monitoring, integrate VirusTotal to catch malicious files, and set up automated scripts to stop attacks immediately.

----
## Tools Used

* Wazuh SIEM Platform: Centralized security manager and endpoint agent used for log collection, monitoring, and alerting.
* VirusTotal API: Threat intelligence integration used to automatically cross-reference file hashes and scan for malware.
* VMware: The virtualization platform (hypervisor) used to host and run the lab environment virtual machines.
* Bash Shell: Used to create the custom script for automatic file removal on the Linux agent.

----
## Project Steps

### 1. Lab Deployment & Agent Registration:
* Deployed the Wazuh Server and Wazuh Agent as virtual machines using VMware.
* Verified network connectivity and successfully registered the endpoint agent to the centralized manager.

### 2. File Integrity Monitoring (FIM) Configuration:
* Configured FIM settings on the Wazuh Server to monitor critical directories on the endpoint.
* Enabled real-time auditing to track and alert on unauthorized file creations, modifications, and deletions.

### 3. Threat Intelligence Integration:
* Integrated the VirusTotal API directly into the centralized Wazuh manager configuration.
* Automated the process of scanning and cross-referencing endpoint file hashes against global threat intelligence.

### 4. Active Response Automation:
* Activated the Active Response capabilities within the Wazuh ecosystem.
* Implemented a custom script to automatically contain and mitigate threats on the endpoint immediately after a rule triggers.
----
## Key Findings
* Real-Time Modification Alerts: Every time an unauthorized file change or creation occurred in the monitored directories, the Wazuh Server instantly caught it and generated a high-severity alert.

* Automated Malware Detection: When a malicious test file was introduced to the endpoint, the VirusTotal integration successfully extracted its hash, cross-referenced it with global threat data, and automatically flagged it as malware.

* Instant Incident Mitigation: Within seconds of the malware detection alert firing, the custom Active Response script triggered automatically on the endpoint. It successfully isolated or removed the threat, proving that the system can contain attacks instantly without waiting for a manual analyst intervention.

----
## Screenshots
To provide visual evidence and clarity, here are screenshots from the Wazuh manager demonstrating the lab configuration, key results, and detection findings.


* Initial Agent Deployment Setup.
<p aligment="center">
<img width="650" height="auto" alt="create agent" src="https://github.com/user-attachments/assets/9f95b007-ec6e-4bd1-bb35-2456ca80d53d" />
<img width="650" height="auto" alt="agent" src="https://github.com/user-attachments/assets/e6a060a6-d1a3-46ff-9763-3f2f34c97291" />
</p>

* Configuring File Integrity Monitoring (FIM) on the Wazuh Agent.
<img width="650" height="auto" alt="file intigrity" src="https://github.com/user-attachments/assets/e0b49cb6-de45-4fbe-818a-9b34cde3e709" />

* Wazuh event dashboard displaying an alert for a file added to the monitored /tmp/malware directory, confirming the File Integrity Monitoring setup.
<p aligment="center">
<img width="650" height="auto" alt="file detection" src="https://github.com/user-attachments/assets/59d97cd6-d4a5-484a-9daf-2765e98e2ea3" />
</p>

* Configuring VirusTotal Integration in the Wazuh Manager.
  <p aligment="center">
    <img width="650" height="auto" alt="virus total setup" src="https://github.com/user-attachments/assets/90ddae92-1adf-4a0e-89b1-74674f413bbb" />
  </p>
  
* Simulating a Threat Using the EICAR Test File to Verify VirusTotal Integration
  <p aligment="center">
  <img width="650" height="auto" alt="image" src="https://github.com/user-attachments/assets/2fb9d726-7fe4-451b-bb1a-e0ea7e30e86d" />
  <img width="650" height="auto" alt="virus total detection" src="https://github.com/user-attachments/assets/522fa160-f7bf-4663-bc1c-db26a78a0139" />
  </p>

  * Configuring the Custom Active Response Script for Automated Mitigation
    <P aligment="center">
      <img width="650" height="auto" alt="image" src="https://github.com/user-attachments/assets/3b4b1000-7cf4-407c-80ac-85ad1d479652" />
    </P>


<p><
<img width="650" height="auto" alt="image" src="https://github.com/user-attachments/assets/2fb9d726-7fe4-451b-bb1a-e0ea7e30e86d" />
</p>


  
