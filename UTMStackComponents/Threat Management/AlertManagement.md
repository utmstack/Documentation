---
layout: default
title: Alert Management
parent: Threat Management
nav_order: 1
---


# Alert Management
Welcome to the Alert Management Section. This resource provides comprehensive guidelines to aid your understanding and usage of our Alert Management system. It covers all the aspects and functionalities of the system, including correlation rules, alert generation, severity assignment, and visualizations, among others.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/AlertDashboard.PNG">

## Introduction
Alert Management is a critical component of any security information and event management (SIEM) system. Its primary function is to monitor various data sources, identify anomalies and suspicious activities, and generate alerts based on predefined correlation rules. It enables organizations to take prompt and effective action against potential threats, ensuring the integrity and safety of their digital assets.

Our Alert Management system features an advanced correlation engine, which is responsible for the generation of alerts. The engine scrutinizes the incoming data in real-time and matches it against the defined correlation rules, the engine generates an alert and assigns it a severity based on the potential impact and threat level of the incident.

The Alert Management Module forms an integral part of our system, serving as a real-time hub for all the alerts detected by the correlation engine. It efficiently captures, displays, and manages vital information related to these alerts, enhancing your capacity to oversee and control potential risks within your environment. With a myriad of features and capabilities, it facilitates better understanding and management of alerts.

## 1. Data Grid
Here, you'll find a comprehensive list of all alerts detected by our powerful correlation engine. This detailed grid, populated in real-time, houses the most relevant and significant alert information such as:

* **Rule Name**: The specific rule that triggered the alert.
* **Severity**: The level of seriousness or urgency attached to the alert.
* **Status**: The current state of the alert, indicating whether it's new, under review, or resolved.
* **Sensor**: The specific source or detector that identified the potential risk, generating the alert.

With a focus on flexibility and ease of use, the Data Grid allows you to sort alerts based on any field. By default, it organizes alerts chronologically, ensuring that you are always up-to-date with the latest alerts raised by the system. Through this streamlined, interactive interface, you can swiftly navigate and respond to the complex alert landscape, bolstering your system's defense capabilities.

### Key Alert Operations
In addition to browsing and sorting alerts, the Alert Management Module allows you to perform three vital operations, which offer deeper insight and aid in effective threat management:

### Creating an Incident Based on an Alert

When an alert signifies a significant threat, warranting further investigation or action, you can use the 'Create Incident' operation. This feature enables you to create a new incident directly from the alert, or associate the alert with an existing incident. The newly created incident will appear in the Incident Module.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/incidentmenu.png">

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/createincident.png">

To learn more about managing incidents, please refer to our detailed guide here.

### Creating a New Tag Rule Based on an Alert
The Alert Management Module also allows you to create a new Tag Rule using the fields of the alert. With this operation, you can define the specific fields needed to automatically tag similar alerts in the future. By default, you'll have the "False Positive" tag available for use.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/tagrule.png">


### Creating Filters from an Alert
The Alert Management Module also provides an intuitive feature to generate a filter based on the specific attributes of an alert. This feature can be particularly helpful when investigating a series of related alerts or when you wish to monitor alerts with similar characteristics.

To utilize this feature, simply select the alert that exhibits the characteristics you wish to filter by. Then, choose the filter icon from Alert' s option.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/filterbyAlert.png">

### Adding Notes to an Alert
To enhance collaboration and knowledge sharing, you can add notes to each alert. This operation enables you to annotate an alert with relevant observations, questions, or insights, providing valuable context for you and your team.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/comment.png">

## 2. Filter

The Filters section provides powerful and customizable functionality to narrow down your view of alerts based on specific criteria. It allows you to interactively filter alerts based on various fields.

For instance, you can focus on 'High Severity' alerts from a specific sensor, or alerts triggered by a particular rule name. To perform a general search across multiple fields, use the search bar at the top.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/filters.png">

The system provides a set of predefined filters, offering a quick start for common filtering needs. However, the Alert Management Module also provides the flexibility to customize these filters. You can add or remove filters according to your specific needs, thereby personalizing the filtering interface to match your operational requirements.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/managefilters.png">

By utilizing the Filters section effectively, you can swiftly navigate the vast array of alerts and focus on those most pertinent to your security objectives. 


## 3. Additional Alert Management Features
The Alert Management Module also offers a variety of additional features to facilitate efficient and personalized alert handling. The 3 Option buttons on the top right of the module contains three main functionalities: Save Report, Manage Tags, and View Tag Rules.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/options.png">


### Save Report

This option allows you to generate and download a report of the alerts in CSV format. The report can be tailored based on a specific timeframe within the last 7 days and the quantity of alerts to be included in the report. The quantity can be predefined as 50, 100, 200, 500, 1000, or 2500 alerts per report, depending on your requirements.

<img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/savereport.png">


### Manage Tags

This function provides the ability to manage and customize the tags available in your system. Tags can be incredibly useful for categorizing and filtering your alerts. You can create new tags or manage existing ones to ensure they align with your alert handling workflow.

  <img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/managetags.png">


### View Tag Rules {#tagginrules}

Finally, the 'View Tag Rules' option allows you to review and manage your established tag rules. In this section, you can inspect the details of each rule or delete them if they're no longer required. Tag rules assist in automating the process of alert tagging based on specific conditions or criteria.

  <img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/managetagrules.png">

  <img alt="dashobard view" src="./../Images/../../Images/Components/ThreatManagment/managetagrules2.png">