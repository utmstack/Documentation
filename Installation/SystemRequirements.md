---
layout: default
title: System Requirements
parent: Installation
nav_order: 2
---

# UTMStack System Requirements
To ensure a smooth installation and optimal performance of UTMStack, it is essential to meet the following system requirements for both the Master and Probe/Proxy servers.

## Master Server Requirements:
The Master server is responsible for managing and coordinating the UTMStack platform. The table below outlines the recommended resource specifications for different environments:


| Environment                   | Cores | RAM  | Disk Space |
| ----------------------------- | ----- | ---- | ---------- |
| Non-prod (minimum required)                     | 4     | 10GB | 74GB       |
| Live Logs (100GB)             | 4     | 16GB | 180GB      |
| **Live Logs (1000GB)**  (most used)          | **16**    | **32GB** | **1080GB**     |
| Cold Data (10000GB)           | 16    | 64GB | 11080GB    |
| Live Logs (10000GB - Cluster) | 16    | 32GB | 1080GB     |


The requirement highlighted is a popular choice among users and widely utilized for most master setups. It has consistently proven to be highly effective based on our experience and user feedback.

Please note that these requirements are the minimum recommendations. For optimal performance, it may be necessary to allocate additional resources based on your specific workload and data volume.


## Probe or Proxy Server Requirements (optional):

A probe, in the context of network monitoring or management, is a crucial component responsible for collecting data and monitoring the status or performance of a network and its components. It operates in a distributed network environment, gathering information and reporting it back to a central management system.

In the case of the probe or proxy server, it serves the purpose of assisting in collecting log data and forwarding it to the master server. This model, allows for efficient management of log data. The probe or proxy server acts as an intermediary, ensuring smooth communication between the data source and the master server.

For the probe or proxy server to effectively fulfill its role, it should meet the following minimum requirements.

{: .important}
Please note that these requirements are specifically applicable when adopting the master and proxy model

| Resource                            | Minimum Requirement       |
| ----------------------------------- | ------------------------ |
| Disk Space for system               | 50 GB                    |
| Cores                               | 4 (May require more)     |
| RAM                                 | 4 GB (May require more)  |

It is important to ensure that the Probe or Proxy server has sufficient disk space, CPU cores, and RAM to handle the data collection and forwarding tasks effectively.

{: .note}
The master can act as probe if a proxy is not used.


## Supported Operating Systems:

The UTMStack installation guide provides instructions specifically for Ubuntu 20.04 LTS and 22.04 LTS. It is recommended to use one of these supported operating systems for compatibility and optimal performance.

Please refer to the installation guide for detailed steps on setting up UTMStack on your chosen operating system.

Ensuring that your system meets these requirements will help guarantee the stability, efficiency, and reliable operation of UTMStack.

If you have any further questions or need additional assistance, please don't hesitate to reach out.


## Federated Server (UTMStackFSInstaller)

### Recommendations for Operating System:
Ubuntu 20.04 LTS.

### Resources for Master:

| Recommendation                | Cores | RAM   | Disk Space |
| ----------------------------- | ----- | ----- | ---------- |
| Minimum Required (non-prod)   | 2     | 4 GB  | 20 GB      |
| Recommended (prod)            | 4     | 8 GB  | 20 GB      |