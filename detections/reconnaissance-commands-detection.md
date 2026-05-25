Reconnaissance Commands Detection

Description

Detects common system and network discovery commands executed on monitored endpoints.

SPL Query

index=* (whoami.exe OR ipconfig.exe OR systeminfo.exe)

Purpose

Monitors reconnaissance activity often performed by attackers during early-stage intrusion activity.

Threat Hunting Goals

* Detect system discovery
* Monitor network enumeration
* Identify attacker reconnaissance behavior

MITRE ATT&CK

* T1033 — System Owner/User Discovery
* T1016 — System Network Configuration Discovery
* T1082 — System Information Discovery
