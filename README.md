# splunk-siem-threat-hunting-lab
Splunk SIEM Threat Hunting Lab

This project demonstrates the deployment and configuration of a SOC-style SIEM environment using Splunk Enterprise, Sysmon, and Windows event telemetry for threat hunting and detection engineering.

The lab environment was built using:

* Ubuntu Desktop VM as the Splunk Enterprise server
* Windows VM as the monitored endpoint
* Sysmon for advanced endpoint telemetry
* Splunk Universal Forwarder for log forwarding

The project focused on:

* Splunk installation and configuration
* Sysmon integration
* Windows event log ingestion
* Threat hunting using SPL queries
* Detection engineering
* MITRE ATT&CK mapping
* Security dashboard creation

Threat hunting activities performed in the lab included:

* User discovery (whoami)
* Account discovery (net user)
* Network discovery (ipconfig)
* System information discovery (systeminfo)
* PowerShell execution monitoring
* Encoded PowerShell command detection

Example SPL detections used:

* index=* EventCode=1
* index=* powershell.exe
* index=* powershell.exe EncodedCommand

MITRE ATT&CK techniques observed:

* T1033 – System Owner/User Discovery
* T1087 – Account Discovery
* T1016 – System Network Configuration Discovery
* T1082 – System Information Discovery
* T1059.001 – PowerShell
* T1027 – Obfuscated/Encoded Files and Information
