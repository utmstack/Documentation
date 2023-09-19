---
layout: default
title: Firewall Rules
parent: Installation
nav_order: 5
---


# Firewall Rules

To ensure proper communication and functionality of UTMStack, it is important to configure the firewall rules on your network devices accordingly. This section provides an overview of the required firewall rules for different components of UTMStack. Please refer to the following guidelines:

## Required Ports

- Port: 22/TCP
  - Purpose: Secure Shell (We recommend creating a firewall rule to allow it only from the admin workstation).

- Port: 80/TCP
  - Purpose: UTMStack Web-based Graphical User Interface Redirector (We recommend creating a firewall rule to allow it only from admin and security analyst workstations).

- Port: 443/TCP
  - Purpose: UTMStack Web-based Graphical User Interface (We recommend creating a firewall rule to allow it only from admin and security analyst workstations).

- Port: 9090/TCP
  - Purpose: Cockpit Web-based Graphical Interface for Servers (We recommend creating a firewall rule to allow it only from the admin workstation).

Other ports will be required during the configuration of UTMStack's integrations to receive logs. Please follow the security recommendations given in the integration guide if it exists.

By configuring the firewall rules as specified above, you ensure that the necessary network traffic is allowed for UTMStack components to function properly. Make sure to update your network devices' firewall settings accordingly to enable seamless communication within the UTMStack environment.
