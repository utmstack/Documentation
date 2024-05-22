---
layout: default
title: False Positive
parent: Threat Management
nav_order: 1
---

# False Positives in Alert Management

In the realm of cybersecurity, not all alerts are indicative of genuine threats. Sometimes, alerts are triggered by benign activities or known behaviors which, while meeting the conditions of an alert rule, do not represent any malicious intent. Such alerts are termed as "False Positives". 

Managing false positives is crucial for security operations. High numbers of false positives can overwhelm security teams, causing them to potentially overlook real threats. Moreover, consistent false alerts can desensitize teams to alerts in general, increasing the risk of missing genuine threats.

## Understanding the "False Positive" Tag

In the Alert Management Module, users have the ability to tag alerts as "False Positive". Once an alert is tagged as a false positive based on certain conditions, the system will recognize similar future alerts under those conditions as false positives and will not raise them as genuine threats.



## Practical Example: False Positive Tagging

Consider an user that belonw to your organization.The Alert Management System, based on certain conditions, might see unusual activity and raise alerts. However, given that the organization is aware of this benign interaction, these alerts are, in fact, false positives.

To handle such a scenario, the organization can set a false positive rule:

### Step-by-Step Guide to Create a False Positive Tag

1. Navigate to the `Alert Management Data Grid ` section in the Alert Management Module.
2. Select the alert that you can extract the condicions to convert it in a false positive tag rule.
3. Click on `Create New Tag Rule`.

![Tag Rule Creation](./../Images/../../Images/Components/ThreatManagment/falsepositivemenu.png)

1. From the available tags, select "False Positive".
2. 2. Give a `name` and a `description` to the Rule.
3. Set the condition as `Equals` and enter the name of the pc.
4. Save the rule.

Once this rule is saved, any alert generated from activity originating from that PC will automatically be tagged as a false positive, ensuring that the security team is not inundated with unnecessary alerts.

---

By effectively managing false positives, organizations can streamline their threat detection and response processes, ensuring that genuine threats don't go unnoticed.

