Splunk Enterprise Installation on Ubuntu

Environment

* Ubuntu Desktop VM
* Splunk Enterprise

Installation Steps

Update Ubuntu

sudo apt update && sudo apt upgrade -y

Install Splunk

sudo dpkg -i splunk-*.deb

Start Splunk

sudo /opt/splunk/bin/splunk start --accept-license --answer-yes --run-as-root

Access Splunk Web

http://localhost:8000

Outcome

Successfully deployed Splunk Enterprise SIEM on Ubuntu Desktop VM.
