---
layout: default
title: SOC AI Feature
nav_order: 7
---

# SOC AI Feature

## Overview of SOC AI

The SOC AI (Security Operations Center Artificial Intelligence) feature in UTMStack is designed to enhance the efficiency and effectiveness of security operations by automating the analysis and management of alerts. SOC AI continuously monitors incoming alerts, analyzing them along with related logs and reviewing similar past alerts to determine the appropriate actions based on historical data and configurations.

## Key Features of SOC AI

### **Automated Alert Analysis**

SOC AI performs a detailed analysis of each alert and the associated logs. It cross-references current alerts with previous ones to understand the actions taken by security analysts and any false positive tags that were assigned.

### **Configurable Actions**
Based on the investigation, SOC AI can be configured to take one of the following actions:

1. **Close the Alert:**: If SOC AI identifies an alert as a false positive, it can automatically close the alert.
2. **Change Alert Status to In Review**: If an alert requires further attention, SOC AI can mark it as "In Review".
3. **Create an Incident**: For alerts deemed dangerous enough, SOC AI can escalate the alert by creating an incident.

Alternatively, if configured to only investigate:

- **No Status Change:**: SOC AI will not change the alert status or open an incident.
- **Investigation Report**: SOC AI will provide a detailed description of the investigation, findings, and recommendations on how the alert should be treated.

### **Integration with Ticketing Systems**

For optimal performance, SOC AI can be integrated with your ticketing management system. UTMStack can be configured to send emails to your ticketing system whenever a new incident is opened. This ensures that SOC AI's findings and incident creations are seamlessly integrated into your existing workflow, notifying you only when necessary.

### **Continuous Improvement**

SOC AI improves over time as it learns from your interactions. By tagging alerts as false positives and fine-tuning the system, the AI becomes more accurate and efficient in handling alerts, continuously enhancing its performance based on your feedback.

## Setting Up SOC AI

To maximize the benefits of SOC AI, proper configuration is essential. Here are the steps to set up SOC AI in UTMStack:

1. **Access SOC AI Settings:** Navigate to the SOC AI settings in the UTMStack dashboard.
2. **Configure Alert Actions:** Decide whether SOC AI should automatically close false positives, change alert statuses, or create incidents based on its analysis.
3. **Integrate with Ticketing System:** Set up email notifications to your ticketing management system for seamless incident management.
4. **Train SOC AI:** Regularly tag alerts as false positives and adjust settings to help SOC AI learn and improve its accuracy.

## Conclusion

SOC AI in UTMStack is a powerful tool that automates the monitoring, analysis, and management of security alerts. By leveraging historical data and continuous learning, SOC AI enhances the efficiency of your security operations, ensuring that only the most critical issues demand your attention. Proper configuration and integration with your ticketing system can significantly improve your incident response and overall security posture.
For further details on configuring SOC AI, refer to the UTMStack user manual or contact our support team.
