Sysmon Installation and Configuration

Objective

Deploy Sysmon to collect advanced Windows endpoint telemetry.

Tools Used

* Sysmon
* SwiftOnSecurity Sysmon Configuration

Installation Command

Sysmon64.exe -accepteula -i sysmonconfig-export.xml

Validation

Get-Service Sysmon64

Outcome

Successfully enabled advanced endpoint telemetry including:

* Process creation
* Network connections
* DNS queries
* Registry modifications
