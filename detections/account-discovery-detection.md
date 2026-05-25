Account Discovery Detection

Description

Detects account enumeration activity using the net user command.

SPL Query

index=* net.exe

Purpose

Monitors account discovery behavior commonly associated with attacker reconnaissance.

MITRE ATT&CK

* T1087 — Account Discovery
