---
layout: default
title: System Requirements
parent: Installation
nav_order: 3
---

# UTMStack System Resources

To guarantee a seamless installation and peak performance of UTMStack, adhere to the given system specifications for both Master and Probe/Proxy servers.

Before diving in, be aware that UTMStack approaches data retention in two distinct methods:

* **Hot Log Storage**: Refers to data which isn't archived and can be accessed anytime for immediate analysis.
* **Cold Storage**: Represents archived data that necessitates restoration prior to access.
* **Data Source**: Denotes any individual origin of logs, such as devices, agents, or SaaS integrations.

## Assumptions:

It's assumed that 60 data sources (devices) roughly produce 100 GB of data monthly.

## Master Server Specifications:

The Master server undertakes the task of overseeing and orchestrating the UTMStack platform. Below is a tabulation of the recommended specifications for the **hot log storage**:

| Data Sources (Approx. Monthly Data) | Cores | RAM   | Disk Space |
| ----------------------------------- | ------| ------| -----------|
| **50 (100 GB)**                     | 4     | 8 GB  | 150 GB    |
| **120 (250 GB)**                    | 8     | 16 GB | 250 GB    |
| **240 (500 GB)**                    | 16    | 32 GB | 450 GB    |

You have the flexibility to mix and match these tiers based on the number of devices you have and your preferred hot log storage duration.

## Supported Operating Systems:

The UTMStack installation guide provides instructions specifically for Ubuntu 22.04 LTS. It is recommended to use one of these supported operating systems for compatibility and optimal performance.

Please refer to the installation guide for detailed steps on setting up UTMStack on your chosen operating system.

Ensuring that your system meets these requirements will help guarantee the stability, efficiency, and reliable operation of UTMStack.

If you have any further questions or need additional assistance, please don't hesitate to reach out.

## Federated Server (UTMStackFSInstaller)

### Recommendations for Operating System:
Ubuntu  22.04 LTS.

### Resources for Master:

| Recommendation                | Cores | RAM   | Disk Space |
| ----------------------------- | ----- | ----- | ---------- |
| Minimum Required (non-prod)   | 2     | 4 GB  | 20 GB      |
| Recommended (prod)            | 4     | 8 GB  | 20 GB      |