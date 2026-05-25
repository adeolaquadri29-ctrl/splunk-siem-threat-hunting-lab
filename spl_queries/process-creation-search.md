Process Creation Hunting

SPL Query

index=* EventCode=1

Purpose

This query detects process creation activity from Sysmon logs.

Use Cases

* Detect suspicious processes
* Investigate attacker execution
* Analyze parent-child relationships
* Monitor command execution

Relevant Sysmon Event

* Event ID 1 — Process Creation
