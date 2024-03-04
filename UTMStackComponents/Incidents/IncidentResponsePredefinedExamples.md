---
layout: default
title: Examples playbooks
parent: Incident Management
nav_order: 4
---

# Examples of incident response playbooks
In this section, we offer **examples of incident response playbooks tailored for Ubuntu systems**, designed to assist system administrators and security professionals in effectively managing security incidents.

## Shutdown Machine

**Use Case:**  
An alert is triggered indicating a high-severity unauthorized access attempt to a critical server. The protocol used is SSH, and the intrusion detection system generated the alert. The source of the attempt is identified with a hostname of `attacker.example.com`, an IP address of `192.0.2.1`, and is coming from the US with ASN 12345 on port 22. 

**Response:**  
```bash
shutdown -h now
```

## Block User
**Use Case:**
An alert for a brute force attack is generated due to multiple failed login attempts via SSH. The alert is active, with high severity, and the source is attacker.example.com from IP 192.0.2.1 in the US with ASN 12345 on port 22.

**Response:**

```bash
usermod -L ${source.user}
```

## Block IP
**Use Case**
Suspicious network traffic is detected by the firewall, triggering an alert categorized as network scanning with high severity. The traffic is on TCP protocol from scanner.example.com with IP 192.0.2.1 from CN with ASN 23456 on port 80.

**Response:**

```bash
iptables -A INPUT -s ${source.ip} -j DROP
```

## Block IP in Firewall

**Use Case:**
An alert of high-severity suspicious firewall traffic categorized as network scanning is triggered. The alert indicates traffic from scanner.example.com with IP 192.0.2.1 from CN with ASN 23456 on port 80.

**Response:**

``` bash
# Connection to the firewall
ssh admin@firewall.example.com

# Command to block the IP in ufw firewall
ufw deny from ${source.ip}
```