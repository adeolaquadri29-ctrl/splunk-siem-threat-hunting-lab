# splunk-siem-threat-hunting-lab

Overview

This project demonstrates the deployment and configuration of a SOC-style SIEM environment using Splunk Enterprise, Sysmon, and Windows event telemetry for threat hunting and detection engineering.

The lab was built to simulate real-world SOC monitoring workflows, endpoint telemetry collection, and security event analysis using Splunk SPL queries and Sysmon logs.

The environment was deployed using:

* Ubuntu Desktop VM as the Splunk Enterprise SIEM server
* Windows VM as the monitored endpoint
* Sysmon for advanced endpoint telemetry
* Splunk Universal Forwarder for centralized log forwarding

⸻

Objectives

* Deploy Splunk Enterprise SIEM on Ubuntu
* Configure Windows log forwarding using Splunk Universal Forwarder
* Integrate Sysmon endpoint telemetry into Splunk
* Perform threat hunting using SPL queries
* Create basic detection engineering workflows
* Map observed behaviors to MITRE ATT&CK techniques
* Build foundational SOC monitoring dashboards

⸻

Technologies Used

Technology	Purpose
Splunk Enterprise	SIEM platform
Sysmon	Windows endpoint telemetry
Splunk Universal Forwarder	Log forwarding
Ubuntu Desktop VM	Splunk server
Windows VM	Monitored endpoint
SPL (Search Processing Language)	Threat hunting and detections

⸻

Lab Architecture

+----------------------+
|     Windows VM       |
|----------------------|
| Sysmon               |
| Splunk Forwarder     |
+----------+-----------+
           |
           | Windows Event Logs
           v
+----------------------+
|     Ubuntu VM        |
|----------------------|
| Splunk Enterprise    |
| Threat Hunting       |
| Dashboards           |
| Detection Rules      |
+----------------------+

⸻

Sysmon Telemetry Collected

The following telemetry was successfully ingested into Splunk:

* Process Creation (Event ID 1)
* PowerShell Execution
* Encoded PowerShell Commands
* Windows Security Logs
* User and System Discovery Commands

⸻

Threat Hunting Activities

The following activities were executed and analyzed within Splunk:

Activity	Purpose
whoami	User discovery
net user	Account discovery
ipconfig	Network discovery
systeminfo	System information discovery
PowerShell Get-Process	PowerShell monitoring
Encoded PowerShell Command	Obfuscation detection

⸻

Example SPL Queries

Process Creation Detection

index=* EventCode=1

PowerShell Activity Detection

index=* powershell.exe

Encoded PowerShell Detection

index=* powershell.exe *EncodedCommand*

Reconnaissance Command Hunting

index=* (whoami.exe OR ipconfig.exe OR systeminfo.exe)

⸻

MITRE ATT&CK Mapping

Activity	MITRE Technique	Description
whoami	T1033	System Owner/User Discovery
net user	T1087	Account Discovery
ipconfig	T1016	System Network Configuration Discovery
systeminfo	T1082	System Information Discovery
powershell.exe	T1059.001	PowerShell
EncodedCommand	T1027	Obfuscated/Encoded Files and Information

⸻

Detection Engineering

Basic detections were created for:

* Process creation monitoring
* PowerShell execution
* Encoded PowerShell commands
* Reconnaissance commands
* Account discovery behavior

Detection logic was implemented using Splunk SPL searches.

⸻

Log Forwarding Configuration

Windows logs were forwarded to Splunk Enterprise using Splunk Universal Forwarder configured with:

* outputs.conf
* inputs.conf

Sysmon Operational logs and Windows Security logs were successfully ingested into Splunk indexes.

⸻

Validation

The following validations were successfully completed:

* Splunk Enterprise installation
* Sysmon deployment and configuration
* Universal Forwarder connectivity
* Windows event log ingestion
* Threat hunting searches
* Detection query execution
* MITRE ATT&CK mapping

⸻

Skills Demonstrated

* SIEM Deployment
* Splunk Administration
* Sysmon Integration
* Windows Event Log Analysis
* Threat Hunting
* SPL Query Development
* Detection Engineering Fundamentals
* MITRE ATT&CK Mapping
* SOC Monitoring Workflows

⸻

Future Improvements

Planned future enhancements include:

* SOC dashboard improvements
* Advanced detection engineering
* Sigma rule integration
* SOAR-lite automation
* Threat intelligence enrichment
* Cloud security monitoring
* Security Onion integration

⸻
