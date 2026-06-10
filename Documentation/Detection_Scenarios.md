# Detection Scenarios

## Overview

A series of attack simulations and security monitoring activities were performed to validate telemetry collection, alert generation, MITRE ATT&CK mapping, and threat hunting workflows within the homelab environment.

---

## Scenario 1 – PowerShell Execution Detection

Objective:
Validate the collection and analysis of PowerShell activity.

Activity:
A PowerShell command was executed on the Windows 11 endpoint.

Outcome:
Sysmon recorded the execution and the event was successfully collected by Wazuh for investigation.

---

## Scenario 2 – Encoded PowerShell Detection

Objective:
Simulate potentially suspicious PowerShell execution behaviour.

Activity:
A Base64-encoded PowerShell command was executed.

Outcome:
The activity was successfully captured and made available for investigation through the Wazuh platform.

---

## Scenario 3 – Local User Creation Detection

Objective:
Validate monitoring of account creation activity.

Activity:
A new local user account was created on the Windows endpoint.

Outcome:
Windows Security events were generated and successfully collected by Wazuh.

MITRE ATT&CK:

* T1098 – Account Manipulation

---

## Scenario 4 – Account Discovery Detection

Objective:
Validate monitoring of account enumeration activity.

Activity:
Native Windows account discovery commands were executed.

Outcome:
Wazuh generated alerts associated with account discovery behaviour.

MITRE ATT&CK:

* T1087 – Account Discovery

---

## Scenario 5 – Agent Disconnection Detection

Objective:
Validate monitoring of endpoint visibility and agent status.

Activity:
The Wazuh agent connection was interrupted during testing.

Outcome:
Wazuh generated an alert indicating loss of agent connectivity.

MITRE ATT&CK:

* T1562.001 – Disable or Modify Tools

---

## Scenario 6 – False Positive Investigation

Objective:
Investigate potentially suspicious activity and determine legitimacy.

Activity:
Windows Update generated DLL-related alerts that initially appeared suspicious.

Outcome:
The activity was analysed and determined to be legitimate Windows behaviour.

---

## Scenario 7 – PowerShell File Download Detection

Objective:
Simulate a file download activity commonly associated with malware delivery.

Activity:
PowerShell was used to download a file to the Windows endpoint.

Outcome:
A high-severity Wazuh alert was generated and mapped to MITRE ATT&CK.

MITRE ATT&CK:

* T1105 – Ingress Tool Transfer

---

## Summary

The scenarios successfully validated log collection, alert generation, threat hunting workflows, and ATT&CK-mapped detections within the SIEM environment.

