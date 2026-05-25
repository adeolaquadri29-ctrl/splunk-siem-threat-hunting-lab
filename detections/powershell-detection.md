PowerShell Detection

Description

This detection identifies PowerShell execution activity within the environment.

SPL Query

index=* powershell.exe

Purpose

Detects PowerShell usage for threat hunting and behavioral monitoring.

Threat Hunting Goals

* Identify suspicious PowerShell execution
* Detect administrative scripting
* Investigate attacker tradecraft

MITRE ATT&CK

* T1059.001 — PowerShell
