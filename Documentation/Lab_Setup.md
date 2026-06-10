# Lab Setup

## Objective

The objective of this project was to build a Security Information and Event Management (SIEM) homelab capable of collecting endpoint telemetry, generating security alerts, mapping detections to the MITRE ATT&CK framework, and supporting threat hunting activities.

## Environment

The lab was implemented using VirtualBox and consisted of the following virtual machines:

### Windows 11

Purpose:

* Monitored endpoint
* Sysmon telemetry generation
* Wazuh agent deployment

Components:

* Sysmon
* Wazuh Agent
* Windows Event Logging

### Ubuntu Server

Purpose:

* Centralized SIEM platform

Components:

* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard

### Kali Linux

Purpose:

* Attack simulation
* Security testing

Tools:

* Nmap
* PowerShell-based testing activities

### Metasploitable

Purpose:

* Prepared for future vulnerability assessment and attack simulation activities

## Log Collection Flow

Windows 11 generated Sysmon and Windows Security events.

The Wazuh agent collected the telemetry and forwarded it to the Wazuh Manager running on Ubuntu Server. Events were indexed and visualized through the Wazuh Dashboard, where threat hunting and alert investigations were performed.

## Outcome

The completed environment successfully collected endpoint telemetry, generated alerts, supported MITRE ATT&CK mapping, and enabled practical threat hunting activities.

