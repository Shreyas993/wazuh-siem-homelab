# Threat Hunting

## Overview

Threat hunting activities were conducted using the Wazuh Dashboard to investigate security events generated during attack simulations and monitoring activities.

The objective was to validate telemetry collection, confirm alert accuracy, and gain practical experience investigating security events within a SIEM environment.

## Data Sources

The following data sources were used during investigations:

* Sysmon events
* Windows Security logs
* Wazuh agent telemetry
* MITRE ATT&CK mapped alerts

## Hunting Activities

### PowerShell Activity Analysis

PowerShell execution events were reviewed to validate that command execution telemetry was being collected correctly.

### Account Activity Investigation

User account creation and account manipulation events were analysed to confirm that Windows Security events were successfully collected and correlated.

### Account Discovery Investigation

Native Windows discovery commands were investigated to validate ATT&CK-mapped detections associated with account enumeration behaviour.

### Agent Status Monitoring

Wazuh agent connectivity alerts were reviewed to verify endpoint visibility and monitoring coverage.

### False Positive Analysis

Potentially suspicious DLL-related alerts were investigated and validated as legitimate Windows Update activity.

## Results

Threat hunting activities confirmed that relevant endpoint telemetry was being collected and that alerts could be effectively investigated through the Wazuh Dashboard.

The exercises also demonstrated how ATT&CK mapping can assist analysts in understanding the context of security events and attacker behaviour.

