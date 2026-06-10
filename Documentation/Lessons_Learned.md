# Lessons Learned

## Overview

This project provided practical experience in designing, deploying, and operating a SIEM homelab environment using Wazuh, Sysmon, Windows 11, and Kali Linux.

Throughout the project, several technical and operational lessons were learned.

## Technical Lessons

### Telemetry Collection Is Critical

Effective monitoring depends on reliable telemetry collection. Proper Sysmon configuration and Wazuh agent connectivity were essential for generating meaningful security visibility.

### Logging Does Not Equal Detection

The presence of logs does not automatically result in alerts. Detection capabilities depend on correlation rules, event processing, and alert logic.

### Time Synchronization Matters

Differences in system time complicated event validation and investigation activities. Consistent timestamps are important for accurate analysis.

## Security Lessons

### MITRE ATT&CK Adds Valuable Context

ATT&CK mapping provided a structured method for understanding attacker behaviour and classifying security events.

### False Positives Require Investigation

Several alerts initially appeared suspicious but were ultimately determined to be legitimate system activity. This highlighted the importance of analyst validation.

### Endpoint Visibility Improves Detection Capability

Sysmon significantly increased endpoint visibility compared to default Windows logging alone.

## Operational Lessons

### Troubleshooting Is Part of Security Operations

Issues involving agent connectivity, event collection, and dashboard visibility required systematic troubleshooting and validation.

### Documentation Improves Project Quality

Maintaining screenshots, investigation notes, and scenario documentation made it easier to track progress and explain findings.

## Conclusion

This project strengthened practical skills in SIEM administration, endpoint monitoring, threat hunting, security investigation, and MITRE ATT&CK-based analysis. It also provided a deeper understanding of how security monitoring platforms operate within a SOC environment.

