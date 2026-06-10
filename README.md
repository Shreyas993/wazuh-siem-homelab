# Wazuh SIEM Homelab

## Overview
This project demonstrates the implementation of a Security Information and Event Management (SIEM) homelab using Wazuh, Sysmon, Windows 11, and Kali Linux. The objective was to simulate common attacker techniques, collect endpoint telemetry, generate security alerts, and perform threat hunting using MITRE ATT&CK mapped detections.

The lab environment was configured with a Windows 11 endpoint running Sysmon and the Wazuh agent, a dedicated Wazuh server for log collection and analysis, and a Kali Linux machine for attack simulation. Multiple attack scenarios were executed, including PowerShell activity, account manipulation, account discovery, agent disconnection, and file download activity. The resulting telemetry was analysed through the Wazuh dashboard to validate detections and investigate security events.

This project provided practical experience in endpoint monitoring, log analysis, threat hunting, SIEM administration, and security event investigation.

## Lab Environment
The homelab environment consisted of three primary virtual machines running in VirtualBox:

* **Windows 11** – Configured as the monitored endpoint. Sysmon was installed to generate detailed telemetry and the Wazuh agent was configured to forward logs to the SIEM platform.
* **Ubuntu Server** – Hosted the Wazuh platform, including the Wazuh Manager, Indexer, and Dashboard components for log collection, analysis, and visualization.
* **Kali Linux** – Used to simulate attacker activity and perform security testing within the lab environment.

The Windows endpoint and Wazuh server were connected through a private virtual network to enable secure log collection and monitoring. Sysmon events, Windows Security events, and Wazuh agent telemetry were collected and analysed through the Wazuh Dashboard for threat detection and investigation.

An additional **Metasploitable** virtual machine was prepared for future vulnerability assessment and attack simulation activities; however, it was not used in the detection scenarios documented in this project.

## Technologies Used
### Virtualization

* Oracle VirtualBox

### Operating Systems

* Windows 11
* Ubuntu Server
* Kali Linux
* Metasploitable (prepared for future testing)

### Security Monitoring

* Wazuh
* Sysmon

### Threat Hunting & Analysis

* Wazuh Dashboard
* MITRE ATT&CK Framework

### Networking & Security Tools

* Nmap
* Windows Event Viewer
* PowerShell
* Command Prompt

### Documentation

* GitHub
* Draw.io

## Dashboard Overview
The Wazuh Dashboard served as the central interface for monitoring, alert analysis, and threat hunting activities throughout the project. Security events collected from the Windows 11 endpoint were forwarded to the Wazuh server, where they were indexed, correlated, and visualized.

The dashboard provided visibility into:

* Endpoint status and agent health
* Security event trends
* Alert severity distribution
* MITRE ATT&CK mapped detections
* Threat hunting investigations
* Security event analysis and validation

The screenshots included in this repository demonstrate the operational dashboard views used during alert monitoring and investigation activities.

## MITRE ATT&CK Mapping
The Wazuh platform was used to correlate security events with the MITRE ATT&CK framework, providing additional context for detection and investigation activities. During testing, multiple attack simulations generated alerts that were automatically mapped to ATT&CK tactics and techniques.

Examples of mapped detections included:

| Technique ID | Technique               | Tactic              |
| ------------ | ----------------------- | ------------------- |
| T1087        | Account Discovery       | Discovery           |
| T1098        | Account Manipulation    | Persistence         |
| T1105        | Ingress Tool Transfer   | Command and Control |
| T1562.001    | Disable or Modify Tools | Defense Evasion     |

The ATT&CK framework provided a structured method for understanding attacker behaviour and validating that security events were being properly classified within the SIEM environment.

## Detection Scenarios

## Threat Hunting Activities

## Challenges Encountered

## Lessons Learned

## Future Improvements
