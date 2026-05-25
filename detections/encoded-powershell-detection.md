Encoded PowerShell Detection

Description

Detects encoded PowerShell commands commonly used for obfuscation and malicious script execution.

SPL Query

index=* powershell.exe *EncodedCommand*

Purpose

Identifies potentially malicious or obfuscated PowerShell activity.

Threat Hunting Goals

* Detect malware execution
* Identify obfuscated commands
* Monitor suspicious scripting activity

MITRE ATT&CK

* T1027 — Obfuscated/Encoded Files and Information
* T1059.001 — PowerShell
