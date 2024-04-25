---
layout: default
title: Upgrade Federation Service
parent: Upgrade
nav_order: 5
---

# UTMStack Federation Service Installation Guide

Welcome to the installation page for the Federated Master Deployment of UTMStack! If you're an MSP (Managed Service Provider) with the mission of managing multiple instances of UTMStack across various customer networks, you're in the right place. Our federated master deployment model is meticulously designed to provide a streamlined management experience, presenting a holistic view of activities across multiple clients and organizations.

This guide will walk you through the process of installing the UTMStack Federation Service (UTMStackFS) on an Ubuntu 20.04 LTS system. Please follow the steps below to ensure a successful installation.

{:note}
For more details contact Customer Service.

## Preparing for Installation

1. Update the package list on your system:

```bash
sudo apt update
```

2. Install the necessary dependencies, including wget and net-tools:

``` bash
sudo apt install wget net-tools
```

3. Download the latest version of the UTMStackFS installer from the official GitHub repository. You can use the following command to retrieve the installer:

``` bash
wget https://github.com/utmstack/UTMStackFSInstaller/releases/download/v10.0.0/UTMStackFSInstaller.zip
```

4. Unzip the installer package using the following command. If you don't have the unzip tool installed, you can do so by running sudo apt-get install zip unzip:

``` bash
unzip UTMStackFSInstaller*.zip
```

5. Set execution permissions for the installer script:

``` bash
cd UTMStackFSInstaller
sudo chmod +x utm_fs_installer.sh
```

## Installation Process
6. Execute the installer script to start the installation process:

``` bash
./utm_fs_installer.sh
```

7. Follow the prompts and provide the necessary information during the installation process.

8. Once the installation is complete, you will be provided with the login credentials for the UTMStackFS panel. The default username is admin, and the password is the one you entered during the installation.

9. Access the UTMStackFS panel using your preferred web browser. Enter the IP address or domain name of your server in the browser's address bar.

10. Enter the provided username and password to log in to the UTMStackFS panel.

By following these steps, you will have successfully installed the UTMStack Federation Service (UTMStackFS) on your Ubuntu 20.04 LTS system. You can now access the UTMStackFS panel and begin using it for your cybersecurity needs.