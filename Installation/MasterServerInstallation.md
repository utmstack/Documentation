---
layout: default
title: Master Server Setup Guide
parent: Installation
nav_order: 3
---
# UTMStack Master Server Setup Guide

This guide will walk you through the process of setting up the UTMStack Master Server. The Master Server is the central component of UTMStack and is responsible for managing the security operations and data collection.

## Installation Options
There are two primary ways to install UTMStack on your Master Server:

1. **Linux Installer**: Deploy UTMStack using the UTMStack installer for Ubuntu Linux. This method is suitable for deploying UTMStack on physical servers, network appliances, or virtual machines in Azure, AWS, GCP, or Digital Ocean.

1. **ISO Image**: If needed, you can install an ISO image that includes the operating system and UTMStack components. This method allows for faster deployment in virtualized environments using popular hypervisors such as VMWare, Hyper-V, Proxmox, or OpenStack.

Choose the installation option that best suits your requirements and follow the respective instructions below.


# Linux Installation Guide

This guide will walk you through the process of installing UTMStack on a Linux system using the official installer script. Please follow the steps below to ensure a successful installation.

## Step 1: Prepare the System

Before starting the installation, make sure that your system meets the minimum requirements and is up to date. Run the following commands to update the package list and install the necessary dependencies:

``` bash
sudo apt update
sudo apt install wget
```

## Step 2: Download the Installer Script

Download the latest version of the UTMStack installer script from the official UTMStack website. You can use the following command to retrieve the script:

``` bash
wget http://github.com/AtlasInsideCorp/UTMStackInstaller/releases/latest/download/installer

```

## Step 3: Grant Execution Permissions

Change to the root user to ensure proper execution of the installer script:

``` bash
sudo su
```

Set execution permissions for the installer script using the following command:

``` bash
chmod +x installer
```

## Step 4: Run the Installer

Now, you are ready to run the installer script and begin the installation process.

Execute the installer without parameters:

``` bash
./installer
```


The installer script will take care of downloading the necessary packages.

Please note that the installation process may take some time depending on the system and the options selected.


{: .important}
Trubleshooting:
If you find any errors during the installation, please check the installation log for more details: /var/log/utm-setup.log

{: .note}
You can found the password and other generated configurations in /root/utmstack.yml

## Step 5: Configuration of UTMStack
After successfully installing UTMStack on your servers, it is important to configure the necessary services to ensure proper functionality. This step involves setting up best-practice firewall rulesets to control network traffic effectively. Additionally, you have the option to integrate third-party applications like M365 to enhance UTMStack's capabilities.

To learn more about the specific firewall rules you need to create for UTMStack, please refer to the **<a href="./FirewallRules.md">Firewall Rules</a>** section for detailed instructions.


## Step 6:  Installing and Configuring an SSL/TLS certificate

Go to **<a href="./FirewallRules.md">Configuring an SSL/TLS certificate</a>** section for detailed instructions.

## Step 7: Accessing the UTMStack Platform
Once you have successfully installed the UTMStack master server, you can now access the platform and start using it for your cybersecurity needs. Follow these steps to log in to the UTMStack platform:

Open your preferred web browser.

Enter the HTTPS URL of your server's name or IP address in the browser's address bar. For example, if your server's IP address is 192.168.0.100, you would enter https://192.168.0.100.

Press Enter to load the UTMStack login page.

<img title="UTMStack Installer Capture" alt="UTMStack Installer Capture" src="./Images/Images/../../../Images/UTMStacklogin.png">

Once UTMStack is installed, use admin as the user and the password generated during the installation for the default user to login. You can found the password and other generated configurations in /root/utmstack.

{: .note}
Note: Use HTTPS in front of your server name or IP to access the login page.

Click on the "Sign In" button to authenticate and access the UTMStack platform.


## ISO Image
The ISO Image option provides a bundled package that includes the Ubuntu Linux operating system and UTMStack components. This allows for a smoother installation process, especially in virtualized environments.

### Prerequisites
Before proceeding with the ISO Image installation, ensure that you have the following:

* A supported hypervisor such as VMWare, Hyper-V, Proxmox, or OpenStack.
* The UTMStack ISO Image downloaded and accessible.


### Installation Steps
Follow these steps to install UTMStack using the ISO Image:

Create a new virtual machine in your preferred hypervisor.
Attach the UTMStack ISO Image to the virtual machine.
Configure the virtual machine settings, including CPU, RAM, and disk space allocation.
Start the virtual machine and follow the on-screen instructions to complete the installation.

By following the appropriate installation method outlined above, you can successfully set up the UTMStack Master Server and begin leveraging its powerful security management capabilities.

Please note that additional configuration steps and post-installation tasks may be required. Refer to the UTMStack Master Server Installation Guide for comprehensive instructions and best practices.

Now that the Master Server is installed, you can proceed to the next step, which is installing the UTMStack software on each server in your network.