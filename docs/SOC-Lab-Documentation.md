# SOC Analyst Home Lab Documentation

## 1. Lab Overview

This project is a hands-on SOC analyst home lab built using Wazuh, Ubuntu Server, Windows, and VirtualBox. The environment was designed to simulate core Security Operations Center activities including endpoint monitoring, security event collection, file integrity monitoring, alert analysis, and investigation.

The Ubuntu Server functions as the Wazuh Manager, while a Windows endpoint is monitored through the Wazuh agent. Security telemetry generated on the Windows system is collected by Wazuh and analyzed through the Wazuh Dashboard.

The lab demonstrates an end-to-end security monitoring workflow: deploying and connecting an endpoint agent, generating activity on the endpoint, collecting security telemetry, detecting changes through File Integrity Monitoring, reviewing generated alerts, and investigating the associated events.

## 2. Lab Environment

- Virtualization: VirtualBox
- Wazuh Manager: Ubuntu Server
- Monitored Endpoint: Windows
- Security Platform: Wazuh
- Monitoring: File Integrity Monitoring (FIM)

## 3. Endpoint Integration

The Windows endpoint was enrolled with the Wazuh Manager and verified as successfully communicating with the server.

During the setup process, troubleshooting was performed to resolve issues involving networking, storage configuration, agent communication, and endpoint monitoring.

After connectivity was established, the Windows endpoint successfully transmitted security telemetry to the Wazuh environment.

### Wazuh Agent Status

The Windows endpoint was successfully connected to the Wazuh Manager and reported an active agent status. This confirms that the endpoint was communicating with the Wazuh environment and available for security monitoring.

![Wazuh Agent Status](../screenshots/wazuh-agent-status.png)

## 4. File Integrity Monitoring

File Integrity Monitoring (FIM) was configured to monitor changes occurring on the Windows endpoint.

The monitoring process detected three types of file activity:

- File creation
- File modification
- File deletion

These activities generated security alerts within the Wazuh Dashboard, providing visibility into changes occurring on the monitored endpoint.

## 5. Security Alerts

Testing the FIM configuration generated the following Wazuh alerts:

| Activity | Wazuh Rule | Severity |
|---|---:|---:|
| File Created | 554 | 5 |
| File Modified | 550 | 7 |
| File Deleted | 553 | 7 |

### Wazuh Alert Evidence

The Wazuh Dashboard captured the file activity generated during testing. The alerts provide visibility into file creation, modification, and deletion events detected on the Windows endpoint.

![Wazuh Security Alerts](../screenshots/wazuh-security-alerts.png)
## 6. Alert Investigation

The investigation workflow began by reviewing the generated Wazuh alerts and identifying the activity that triggered each detection.

The investigation involved reviewing:

- Alert severity
- Detection rule
- Event timestamp
- Affected file
- Endpoint activity
- File operation performed

The generated alerts demonstrated how a SOC analyst can use endpoint telemetry to identify and investigate potentially suspicious file activity.

## 7. SOC Workflow Demonstrated

1. Deploy and configure a security monitoring platform
2. Connect a Windows endpoint to the Wazuh Manager
3. Collect endpoint security telemetry
4. Configure File Integrity Monitoring
5. Generate controlled file activity
6. Detect the activity through Wazuh
7. Review security alerts
8. Analyze event details and affected files
9. Document investigation findings

## 8. Skills Demonstrated

- Security Monitoring
- Endpoint Monitoring
- File Integrity Monitoring
- Security Alert Analysis
- Log Analysis
- Incident Investigation
- Wazuh
- Windows Administration
- Linux Administration
- VirtualBox
- Network Troubleshooting
- Technical Documentation

## 9. Project Outcome

The lab successfully demonstrated end-to-end security monitoring between a Windows endpoint and a Wazuh Manager running on Ubuntu Server.

Controlled file activity generated real security alerts for file creation, modification, and deletion, allowing the events to be observed and investigated through the Wazuh Dashboard.

This provided hands-on experience with core SOC analyst responsibilities including endpoint monitoring, security telemetry analysis, alert investigation, troubleshooting, and security documentation.
