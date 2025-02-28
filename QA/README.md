---
layout: default
title: Q&A
nav_order: 8
has_children: false
---

# Q&A Guide

## Uninstalling Client Agents in UTMStack

To ensure a thorough and trouble-free uninstallation of client agents, please execute the steps below:

1. **Uninstalling UTMStack Agent on Windows**:
  
   **Prerequisites**
   - Ensure you have administrative privileges.

   **Steps**:
   1. Open PowerShell as Administrator:
   2. Execute the Uninstallation Command
         ```shell
      Start-Process "C:\Program Files\UTMStack\UTMStack Agent\utmstack_agent_installer.exe" -ArgumentList 'uninstall' -NoNewWindow -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'stop','UTMStackAgent' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'delete','UTMStackAgent' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'stop','UTMStackRedline' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'delete','UTMStackRedline' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'stop','UTMStackUpdater' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'delete','UTMStackUpdater' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'stop','UTMStackWindowsLogsCollector' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'delete','UTMStackWindowsLogsCollector' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'stop','UTMStackModulesLogsCollector' -Wait -ErrorAction SilentlyContinue | Out-Null; Start-Process -FilePath "sc.exe" -ArgumentList 'delete','UTMStackModulesLogsCollector' -Wait -ErrorAction SilentlyContinue | Out-Null; Write-Host "Removing UTMStack Agent dependencies..."; Start-Sleep -Seconds 10; Remove-Item 'C:\Program Files\UTMStack\UTMStack Agent' -Recurse -Force -ErrorAction Stop; Write-Host "UTMStack Agent removed successfully."
      ```

2. **Uninstalling UTMStack Agent on Linux**:
   **Prerequisites**
   - Ensure you have root privileges.
   - Close any running UTMStack processes.

   **Steps**:
   1. Open Terminal:
      - Access the terminal as a user with sudo permissions.
   2. Execute the Uninstallation Command:
      - Copy and paste the following command into the terminal and press Enter:
         ```shell
      sudo bash -c "/opt/utmstack-linux-agent/utmstack_agent_installer uninstall || true; systemctl stop UTMStackAgent 2>/dev/null || true; systemctl disable UTMStackAgent 2>/dev/null || true; rm /etc/systemd/system/UTMStackAgent.service 2>/dev/null || true; systemctl stop UTMStackRedline 2>/dev/null || true; systemctl disable UTMStackRedline 2>/dev/null || true; rm /etc/systemd/system/UTMStackRedline.service 2>/dev/null || true; systemctl stop UTMStackUpdater 2>/dev/null || true; systemctl disable UTMStackUpdater 2>/dev/null || true; rm /etc/systemd/system/UTMStackUpdater.service 2>/dev/null || true; systemctl stop UTMStackModulesLogsCollector 2>/dev/null || true; systemctl disable UTMStackModulesLogsCollector 2>/dev/null || true; rm /etc/systemd/system/UTMStackModulesLogsCollector.service 2>/dev/null || true; systemctl daemon-reload 2>/dev/null || true; echo 'Removing UTMStack Agent dependencies...' && sleep 10 && rm -rf /opt/utmstack-linux-agent && echo 'UTMStack Agent dependencies removed successfully.'"
      ```

## Addressing Alerts Without User Identification in UTMStack

When confronted with alerts missing user IDs, showing "Not available" in the User field, delve into the **original logs**. These logs may contain user information that wasn't captured or parsed correctly during the alert generation process.

## Locating Integration Guides in UTMStack

Integration guides are available in the **Integrations Section** of the application. These guides offer detailed instructions for installing agents with a variety of platforms.

## Understanding the Role of the Probe Server in UTMStack

The Probe server previously part of UTMStack's architecture is now obsolete. The updated system architecture involves **Agents directly installed on devices**, which relay logs to UTMStack, enhancing efficiency and data acquisition.

## Baseline Rules in UTMStack

Baseline rules in UTMStack are critical for setting the standard for expected operational behavior:

- **Definition**: These rules establish the norm for routine operations.
- **Functionality**: Deviations from established norms trigger alerts, prompting further investigation.

For additional insights, refer to the [Correlation Rules](../Correlation%20Rules/README.md) documentation.


## Compliance Features within UTMStack

UTMStack is equipped with an array of compliance features tailored to meet various regulatory requirements:

1. **Health Insurance Portability and Accountability Act (HIPAA)**:
   Aimed at safeguarding sensitive patient data, with reports tailored to enforce HIPAA provisions.

2. **General Data Protection Regulation (GDPR)**:
   Ensures adherence to EU data protection laws with pre-configured compliance reports.

3. **Gramm-Leach-Bliley Act (GLBA)**:
   Assists financial institutions in managing private information through customized reports.

4. **System and Organization Controls 2 (SOC 2)**:
   Offers reports in line with SOC 2’s Control Criteria for non-financial reporting controls.

5. **Federal Information Security Management Act (FISMA)**:
   Includes predefined reports to aid in upholding FISMA regulations.

6. **Cybersecurity Maturity Model Certification (CMMC)**:
   Provides targeted reports for compliance with various CMMC Levels for U.S. Government contract aspirants.

7. **Payment Card Industry Data Security Standard (PCI-DSS)**:
   Features specific reports to ensure credit card data processing is within PCI-DSS guidelines.



## What network and host intrusion detection services does UTMStack offer?
UTMStack offers network and host intrusion detection services that include rule-based network intrusion detection, rule-based host intrusion detection system, and heuristic-based analysis with ATP capabilities, as well as network traffic, protocol, and DNS analysis.

## What access rights audit services does UTMStack offer?
UTMStack offers access rights audit services that include an Active Directory explorer, user activity and permissions tracking, and suspicious activity monitoring.

## What file classification services does UTMStack offer?
UTMStack offers file classification services that include file change and access tracking, activity monitoring, and file integrity monitoring.

## What Deep Web monitoring services does UTMStack offer?
UTMStack offers Deep Web monitoring services that include monitoring for compromised or stolen data from employees and customers, as well as monitoring of domain and individual email addresses.

## How is UTMStack different from other cybersecurity platforms?
UTMStack stands out from other cybersecurity platforms by offering an integrated, cost-effective solution that bundles multiple cybersecurity products on a single platform. This reduces the learning curve for security professionals and the costs of purchasing different tools from multiple vendors. In addition, the platform includes a powerful dashboard and report builder that can be used to customize the monitoring experience or to perform advanced compliance audits and reports.

## For what types of environments is UTMStack designed?
UTMStack is designed for hybrid environments, allowing it to be easily implemented in both on-premises and cloud environments.

## What compliance features does UTMStack include?
UTMStack includes compliance reports for HIPAA, GLBA, SOC, and GDPR, as well as an event and log explorer for advanced forensic analysis and a customizable report/dashboard builder for compliance reporting.

# What threat detection technology does UTMStack use?
UTMStack uses a range of rule-based, scanner, and AI-powered machine learning algorithms for its threat detection engine. The modules operate independently and, in some cases, are combined to provide more accurate and real-time threat detection.

# What log management services does UTMStack offer?
UTMStack offers log management services that include log collection and correlation, customizable correlation rules and integration with third-party log management solutions.

## What data can I define with baseline rules?
We offer baseline rules that allow users to define the following data:
- Whitelist of allowed internal IP addresses
- Whitelist of allowed IP addresses for login
- Whitelist of allowed applications
- Whitelist of allowed O365 users
- Whitelist of allowed Windows users

For an in-depth understanding, visit [Customizable Rules](../Correlation%20Rules/CustomizableRules.md).


## How can I get more information or request additional assistance?
To get more information or request additional assistance, please contact us and we'll be happy to help.


## File Classification Services
UTMStack offers file classification services that include:
- File change and access tracking
- Activity monitoring
- File integrity monitoring

## UTMStack vs. Other Cybersecurity Platforms
UTMStack is unique in that it:
- Provides an integrated, cost-effective cybersecurity solution
- Bundles multiple cybersecurity tools into one platform
- Features a powerful dashboard and report builder for customization
- Reduces learning curves and vendor costs

## Threat Detection Technology
UTMStack's threat detection uses:
- Rule-based algorithms
- Scanner technologies
- AI-powered machine learning algorithms
- Independent and combined module operation for accurate threat detection

## Log Management Services
UTMStack's log management services encompass:
- Log collection and correlation
- Customizable correlation rules
- Integration with third-party log management solutions


## AD Audit Activation Issue
If encountering issues when activating AD Audit in UTMStack v9:
- It's advised to upgrade to the latest version of UTMStack for improved compatibility and performance due to potential incompatibility with Windows updates.

## Instance Integration Limitations
For UTMStack instances:
- A v9 instance cannot be integrated with a v10 instance for archiving or receiving alerts due to compatibility issues.

## Agent Compatibility
Regarding UTMStack agents:
- The v10 agent, deployed via PowerShell, cannot be used with v9. Each version requires the respective agent.
