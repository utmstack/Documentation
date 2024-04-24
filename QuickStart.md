---
layout: default
title: Quick Start
nav_order: 2
---

# Quick Start Guide

Getting started with UTMStack is straightforward. Follow this 3-step process:

1. **Installation**: Deploy UTMStack on your Master Server.
2. **Initial Configuration**: Set up essential settings, including SSL and email configurations.
3. **DataSource Setup**: Configure a Windows Agent as a data source.

## 1. Install UTMStack

Before you begin, ensure your system meets the minimum requirements: **8 cores**, **16 GB of RAM**, and **150 GB of disk storage** to monitor up to **50 devices**.

*** Integration Requirements *** : To ensure optimal system performance, certain additional requirements beyond the minimums must be considered. Each integration being introduced should reserve at least 1GB of space. This reservation is crucial to ensure proper data storage and efficient system operation as a whole.

*** Logging Volume Considerations ***: Furthermore, it's important to take into account the volume of logs generated and processed within 10-minute intervals. If this volume exceeds 1GB within any time interval, immediate communication with the support team is required. This communication is essential to ensure system stability and performance, as well as to address any potential issues related to log management.

Deploy the UTMStack Server, which oversees security operations and data collection.

### **Procedure**:

Use the UTMStack installer for Ubuntu Linux 22.04 LTS.

- **Download and Prepare**:  
    ```bash
    sudo apt update
    sudo apt install wget
    wget http://github.com/utmstack/UTMStack/releases/latest/download/installer
    sudo su
    chmod +x installer
    ```

- **Install**:  
    ```bash
    ./installer
    ```

### **Configure Firewall and Ports**:

Ensure the following ports are correctly configured on your firewall for UTM Stack access:

- **22/TCP**: Secure Shell (Restrict to admin workstation).
- **80/TCP**: Web-based GUI Redirector (Restrict to admin and security analyst workstations).
- **443/TCP**: Web-based GUI (Restrict to admin and security analyst workstations).
- **9090/TCP**: Cockpit Web-based Interface (Restrict to admin workstation).

### Setup SSL with Certbot (Optional, but recommended):
If you haven't manually installed an SSL certificate, use Certbot to generate one for your domain. This ensures encrypted connections for your users.

Follow the provided guide: [Generate SSL with Certbot](./Installation/SSLConfiguration).


## 2. Initial Configuration

Post installation, the first time you get access to UTMStack, its going to be required that enter the old password and establish the new one.The default username is `admin`. Your initial password and other configurations can be found in `/root/utmstack.yml`.
 
 After that you need to configure the email setting
 
###  **Email Configuration**

1. **Access Email Settings**:
    - Navigate to `Settings` > `Email Configuration` within the UTMStack platform.


2. **SMTP Setup**:
- **Mail Server Password**: The password for your email server to authenticate and send out notifications.

- **UTMStack email address**: The official UTMStack email address that will be used to send out notifications.

- **UTMStack base url**: This refers to the primary URL or address through which all users and systems interact with the UTMStack platform.  For example: `https://UTMStack.UTMStack.com`.

- **Mail Server Host**: For example: `example.hostmail.com`.

- **Mail Server Port**: Typically, the port can be `587`.

- **Mail Server Username**: The username for your email server.

- **Encryption type**: Choose the encryption protocol for your email server. Options include:
  - STARTTLS
  - SSL/TLS
  - NONE 

 Refer to the [Email Configuration Section](./UTMStackComponents/Configuration/ApplicationSetting) for a detailed walkthrough.

## 3. Configure a Windows Agent DataSource

Add a Windows agent to forward logs and data to UTMStack.

## Procedure:

### 1. Pre-installation Requirements:
   * **Compatibility:** Ensure the system runs on Windows Server version 2016 R2 or later.
   * **Network:** Ensure ports 9000 and 50051 are open.

### 2. Installation Steps:
   1. Go to `Integrations` and select `Windows Agent`.
   2. Open a Windows PowerShell terminal with "Administrator" privileges and execute the provided command from the instructions.




