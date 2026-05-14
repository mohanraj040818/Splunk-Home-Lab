# Splunk-Home-Lab
A cross-platform SIEM pipeline connecting a Windows 11 endpoint to an Ubuntu Splunk Indexer.
Splunk Home Lab: Cross-Platform SIEM Integration

Project Overview
This project demonstrates a functional Security Operations Center (SOC) pipeline. I successfully integrated a Windows 11 virtual machine as an endpoint, shipping telemetry data to a centralized Splunk Indexer running on Ubuntu 22.04.

Technical Environment
- SIEM: Splunk Enterprise (Ubuntu)
- Endpoint:Windows 11 (Universal Forwarder)
- Network:Port 9997 (TCP)
- Virtualization:Oracle VM VirtualBox

Key Screenshots
1. Network Connectivity
Verified TCP handshake on port 9997 using PowerShell.

2. Backend Configuration
Modified server.conf to enable remote administrative access.

3. Data Ingestion Success
Confirmed 120,000+ events indexed with synchronized timestamps.

Challenges Overcome
- Time Synchronization:Resolved an 8-hour offset by standardizing system clocks to Asia/Kuala_Lumpur.
- Authentication Hardening: Overrode default security settings in `server.conf` to allow remote login from the Windows VM.
- Firewall Management:Configured Ubuntu UFW to permit ingress traffic for real-time log streaming.
