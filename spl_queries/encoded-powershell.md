Encoded PowerShell Detection

SPL Query

index=* powershell.exe *EncodedCommand*

Purpose

Detects obfuscated or encoded PowerShell commands commonly used by attackers.

Threat Hunting Goals

* Detect malware execution
* Identify obfuscated scripts
* Monitor suspicious PowerShell behavior

MITRE ATT&CK

* T1027 — Obfuscated/Encoded Files and Information
* T1059.001 — PowerShell
