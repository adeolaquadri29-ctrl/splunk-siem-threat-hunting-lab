Splunk Universal Forwarder Setup

Objective

Configure Windows log forwarding to Splunk Enterprise.

Forwarder Configuration

outputs.conf

[tcpout]
defaultGroup = default-autolb-group
[tcpout:default-autolb-group]
server = SPLUNK_SERVER_IP:9997

inputs.conf

[WinEventLog://Microsoft-Windows-Sysmon/Operational]
disabled = 0
index = sysmon
renderXml = true
[WinEventLog://Security]
disabled = 0
index = windows

Validation

Restart-Service SplunkForwarder

Outcome

Successfully forwarded Sysmon and Windows Security logs to Splunk Enterprise.
