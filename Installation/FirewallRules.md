---
layout: default
title: Firewall Rules
parent: Installation
nav_order: 5
---

# Firewall Rules

To ensure proper communication and functionality of UTMStack, it is important to configure the firewall rules on your network devices accordingly. This section provides an overview of the required firewall rules for different components of UTMStack. Please refer to the following guidelines:

## Rules for Access from Probe/Proxy to Master

Allow incoming traffic on the following ports from the probe/proxy to the master:

- Port: 1194/TCP
  - Purpose: Used to connect the probe/proxy over the internet using VPN.

## Rules for Access from Master to Probe/Proxy

Allow incoming traffic on the following ports from the master to the probe/proxy:

- Ports: 9390/TCP and 8888/TCP
  - Purpose: Used to connect with the vulnerabilities scanner.

- Ports: 5000/TCP and 8000/TCP
  - Purpose: Used to connect with the assets discovery service.

## Rules for Access from Agentless Devices to Master or Probe/Proxy

Allow incoming traffic on the following ports from agentless devices (firewalls, hypervisors, etc.) to the master or probe/proxy:

- Port: 2055/UDP
  - Purpose: Used to send Netflow packets.

- Port: 514/UDP
  - Purpose: Used to send syslog logs.

- Port: 514/TCP
  - Purpose: Used to send syslog logs.

- Port: 1470/TCP
  - Purpose: Used to send syslog logs.

- Port: 2056/TCP
  - Purpose: Used to send syslog logs.

- Port: 8089/TCP
  - Purpose: Used to send logs through HTTP POST.

## Rules for Agents Communication with Master or Probe/Proxy

Allow incoming traffic on the following ports on the master for agents to communicate with the master or probe/proxy:

- Port: 5044/TCP
  - Purpose: Used to send logs.

- Ports: 1514-1516/TCP
  - Purpose: Used for HIDS agent communications.

- Port: 55000/TCP
  - Purpose: Used for HIDS management API.

- Port: 9000/TCP
  - Purpose: Used to connect to the Agent Manager.

## Rule for Accessing the UTMStack Web Console

Allow incoming traffic on port 443 to access the UTMStack Web console.

By configuring the firewall rules as specified above, you ensure that the necessary network traffic is allowed for UTMStack components to function properly. Make sure to update your network devices' firewall settings accordingly to enable seamless communication within the UTMStack environment.
