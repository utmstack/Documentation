---
layout: default
title: System Requirements
parent: Installation
nav_order: 3
---

# UTMStack System Resources

To ensure a seamless installation and maximum performance of UTMStack, adhere to the system specifications for the UTMStack server.

Before diving in, be aware that UTMStack approaches data retention in two distinct methods:

* **Hot Log Storage**: Refers to data which isn't archived and can be accessed anytime for immediate analysis.
* **Cold Storage**: Represents archived data that necessitates restoration prior to access.
* **Data Source**: Denotes any individual origin of logs, such as devices, agents, or SaaS integrations.

## Assumptions:

It's assumed that 50 data sources (devices) roughly produce 100 GB of data monthly.

## UTMStack Server Specifications:

The server undertakes the task of overseeing and orchestrating the UTMStack platform. Below is a tabulation of the recommended specifications for the **hot log storage**:

| Data Sources (Approx. Monthly Data) | Cores | RAM   | Disk Space |
| ----------------------------------- | ------| ------| -----------|
| **50 (100 GB)**                     | 8     | 16 GB | 150 GB    |
| **120 (250 GB)**                    | 16    | 32 GB | 250 GB    |
| **240 (500 GB)**                    | 32    | 64 GB | 450 GB    |

You have the flexibility to mix and match these tiers based on the number of devices you have and your preferred hot log storage duration.

*** Achitecture Requirements ***
To ensure optimal performance and full compatibility when running UTMStack, the hardware must meet the following specifications:
**CPU: Processor with support for x86-64 v2 architecture.**
It is essential to verify that your system's processor is compatible with this architecture to guarantee the proper functioning of UTMStack.

### Supported CPU Architectures for Virtualized Environments

### CPU configuration in virtualized environments can impact system performance and compatibility. UTMStack supports the following CPU architectures in QEMU/KVM environments:

1.	**86-64-v2** (QEMU): Based on the 64-bit x86 architecture with a second-generation instruction set, offering improved compatibility and optimized performance.
2. **86-64-v2-AES (QEMU)**: Similar to x86-64-v2, but with support for encryption acceleration through the AES-NI (Intel Advanced Encryption Standard New Instructions) instruction set, enhancing security and encryption speed for sensitive applications.
3. **86-64-v4 (QEMU)**: A fourth-generation architecture incorporating a broader set of advanced instructions and performance improvements compared to previous versions.
4. **Host (KVM)**: This option allows the virtual machine to use the host processor’s features directly, maximizing performance and compatibility with specific hardware.

*** Integration Requirements *** : To ensure optimal system performance, certain additional requirements beyond the minimums must be considered. Each integration being introduced should reserve at least 1GB of space. This reservation is crucial to ensure proper data storage and efficient system operation as a whole.

*** Logging Volume Considerations ***: Furthermore, it's important to take into account the volume of logs generated and processed within 10-minute intervals. If this volume exceeds 1GB within any time interval, immediate communication with the support team is required. This communication is essential to ensure system stability and performance, as well as to address any potential issues related to log management.

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
