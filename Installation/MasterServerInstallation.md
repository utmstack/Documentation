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


## Linux Installer

The Linux Installer provides a straightforward method for deploying UTMStack on a Linux server. It supports both virtual machine deployments and installations on physical servers or network appliances.

### Prerequisites

Before proceeding with the installation, ensure that you have reviewed and met the **<a href="./SystemRequirements">System Requirements</a>** for UTMStack.


### Overview of the Installation Steps

After setting up your master server, you can then proceed with installing UTMStack using the official installer script, available from the **[UTMStack Repository](https://github.com/AtlasInsideCorp/UTMStackInstaller)**.

This script will guide you through all necessary steps.

Once done, you will have completed the installation process.

For detailed step-by-step instructions, including the commands involved in the installation process, refer to the **<a href="./LinuxInstallation.md">Linux Installation Guide</a>**.

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