Process Creation Detection

Description

This detection monitors process creation activity using Sysmon Event ID 1 logs ingested into Splunk.

SPL Query

index=* EventCode=1

Purpose

Detects process execution activity across monitored Windows systems.

Threat Hunting Use Cases

* Detect suspicious process execution
* Investigate attacker commands
* Analyze parent-child process relationships
* Monitor endpoint activity

Sysmon Event

* Event ID 1 — Process Creation

MITRE ATT&CK

* T1059 — Command and Scripting Interpreter
