# SOC Tier 1 Investigation: Brute-Force Attack

## Overview

This project documents a simulated SOC Tier 1 investigation into suspicious authentication activity on a Windows file server (FS-01).

Using Splunk Enterprise and Windows Security Event Logs, I investigated repeated failed logons, identified a successful unauthorised login, reconstructed the attack timeline, analysed post-compromise activity, and developed incident response recommendations.

## Objectives

- Investigate suspicious authentication activity.
- Identify suspicious source IP addresses and targeted accounts.
- Distinguish true positives from false positives.
- Reconstruct the attack timeline.
- Investigate post-compromise activity.
- Map observed activity to MITRE ATT&CK.
- Assess incident impact and recommend containment measures.

## Tools Used

- Splunk Enterprise
- Windows Security Event Logs
- SPL (Search Processing Language)
- MITRE ATT&CK

## Investigation Summary

Analysis of 115 security events identified suspicious activity originating from an external IP address within the simulated environment.

The investigation identified:

- Repeated failed authentication attempts against an administrator account.
- Successful Remote Desktop authentication following the failed attempts.
- Discovery activity following account compromise.
- Creation of a new user account.
- Addition of the new account to the Administrators group.
- Security audit log clearing.

The activity was assessed as a true positive and classified as a high-severity incident.

## Investigation Methodology

1. Ingested and verified log data in Splunk.
2. Analysed event distribution by source IP.
3. Identified and investigated the suspicious external IP.
4. Analysed targeted accounts and authentication patterns.
5. Reconstructed the attack timeline.
6. Investigated post-authentication activity.
7. Reviewed internal authentication failures to identify false positives.
8. Mapped observed activity to MITRE ATT&CK.
9. Assessed impact and developed incident response recommendations.

## Skills Demonstrated

- SIEM investigation
- Splunk searching and SPL
- Windows Event Log analysis
- Authentication monitoring
- Brute-force detection
- Alert triage
- Event correlation
- Attack timeline reconstruction
- MITRE ATT&CK mapping
- Incident reporting
- Incident response recommendations

## Outcome

The investigation identified evidence of unauthorised access, privileged account creation, and attempted concealment through security log clearing.

The incident was escalated to the SOC Team Lead with recommendations for containment, investigation expansion, and improved security monitoring.

## Disclaimer

This project is based on a fictional cybersecurity training scenario. All data, systems, accounts, and activity represented in this investigation are simulated and are not associated with a real organisation.
