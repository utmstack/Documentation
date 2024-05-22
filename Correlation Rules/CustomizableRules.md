---
layout: default
title: Customizable Rules
parent: Correlation Rules
nav_order: 3
---

# Customizable Rules

UTMStack allows users to define customizable rules to enhance the monitoring and alerting based on specific requirements of their network environments. 

## Follow these steps:

1. Access the directory where the system correlation rules are located.
<img title="Menu Correleation Rules" alt="Menu Correleation Rules" src="../Images/menu_custom_rules.png" width="500">


2. Select the folder named "custom", intended for custom rules.
<img title="Directory Correleation Rules" alt="Directory Correleation Rules" src="../Images/directory_custom_rules.png">

3. Add, copy, paste or move your customized rules to this folder.
<img title="Create Correleation Rules" alt="Create Correleation Rules" src="../Images/new_custom_rules.png" width="500">


4. Check that they are correctly placed and that their names match the system rules you want to modify.

## Modifying system rules:
If you need to adjust a system rule, simply create a new custom rule with the same name as the system rule you wish to modify. This will allow your custom rule to take precedence over the original system rule. The custom rule must be placed inside the "custom" folder, and if the folder does not exist, it must be created.


## Rule Priority:

Remember that if there is a custom rule and a system rule with the same name, the custom rule will be used instead of the system rule. This ensures that your settings take priority and are applied by the system instead of the default rules.

Below are a few examples of such customizable rules, each tailored for different use-cases:

## 1. Windows: Activity detected from non-whitelisted internal IPs

### YAML Configuration:
```yaml
- name: "Windows: Activity detected from non-whitelisted internal IPs"
  severity: "High"
  description: "Activity has been detected from an IP that is not on the whitelist of allowed internal IPs"
  solution: "We recommend carefully reviewing the logs to verify activity from an IP that is not on the whitelist of allowed internal IPs"
  category: "Connection from non-whitelisted"
  tactic: "Exfiltration"
  dataTypes: ["wineventlog"]
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - allOf:
        - field: "logx.wineventlog.host.ip.*"
          operator: "regexp"
          value: "(^10(.((2([0-4][0-9]|5[0-5]))|(1[0-9]{2})|([1-9]?[0-9]))){3}$|^172(.(1[6-9]|2[0-9]|3[0-1])(.((2([0-4][0-9]|5[0-5]))|(1[0-9]{2})|([1-9]?[0-9]))){2})$|^(192.168|169.254)(.((2([0-4][0-9]|5[0-5]))|(1[0-9]{2})|([1-9]?[0-9]))){2}$|^FE80::)"
        - field: "logx.wineventlog.host.ip.*"
          operator: "not in"
          value: "10.0.2.27,192.168.22.128,fe80::97d1:5df4:10fe:7b8d"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.wineventlog.event_data.SubjectUserName"
          alias: "SourceUser"
        - field: "logx.wineventlog.host.name"
          alias: "DestinationHost"
        - field: "logx.wineventlog.event_data.IpAddress"
          alias: "DestinationIP"
        - field: "logx.wineventlog.event_data.IpPort"
          alias: "DestinationPort"
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
```

###  Example
In this rule, users can define their whitelist of internal IPs. As an example, you have the internal IPs whitelist 10.0.2.27,192.168.22.128,fe80::97d1:5df4:10fe:7b8d Which you can change to your list


## 2. Windows: Detected application that is not in the white list of allowed applications

### YAML Configuration:
```yaml
- name: "Windows: Detected application that is not in the white list of allowed applications"
  severity: "High"
  description: "This alert is generated when an application that is not on the white list of allowed applications is detected."
  solution: "We recommend carefully reviewing the logs to verify applications that are not whitelisted"
  category: "Connection from non-whitelisted"
  tactic: ""
  dataTypes: ["wineventlog"]
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - oneOf:
        - field: "logx.wineventlog.event_data.ProcessName"
          operator: "not regexp"
          value: "(svchost.exe|services.exe|poqexec.exe)"
        - field: "logx.wineventlog.event_data.NewProcessName"
          operator: "not regexp"
          value: "(svchost.exe|services.exe|poqexec.exe)"
        - field: "logx.wineventlog.event_data.ParentProcessName"
          operator: "not regexp"
          value: "(svchost.exe|services.exe|poqexec.exe)"
        - field: "logx.wineventlog.event_data.CallerProcessName"
          operator: "not regexp"
          value: "(svchost.exe|services.exe|poqexec.exe)"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.wineventlog.event_data.SubjectUserName"
          alias: "SourceUser"
        - field: "logx.wineventlog.host.name"
          alias: "DestinationHost"
        - field: "logx.wineventlog.event_data.IpAddress"
          alias: "DestinationIP"
        - field: "logx.wineventlog.event_data.IpPort"
          alias: "DestinationPort"
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
```

###  Example
In this rule, users can define their whitelist of applications that are allowed to be on the servers and have activity. As an example, you have the whitelist of applications (svchost.exe|services.exe|poqexec.exe), which you can change to your list

## 3. Microsoft 365: Login detected from non-whitelisted IP

### YAML Configuration:
```yaml
- name: "Microsoft 365: Login detected from non-whitelisted IP"
  severity: "High"
  description: "A user is trying to login from an IP that is not on the whitelist"
  solution: "We recommend carefully reviewing the logs to verify users attempting to login from an IP that is not on the whitelist"
  category: "Connection from non-whitelisted"
  tactic: ""
  dataTypes: ["o365"]
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - allOf:
        - field: "logx.o365.ClientIP"
          operator: "not in"
          value: "163.225.184.79,92.22.1.40,19.144.24.179,37e4:dd49:a173:02f4:3164:1df0:8849:6ef9"
        - field: "logx.o365.Operation"
          operator: "=="
          value: "UserLoggedIn"
        - field: "logx.o365.ResultStatus"
          operator: "in"
          value: "Success,PartiallySucceeded,True"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.o365.UserId"
          alias: "SourceUser"
        - field: "logx.o365.ClientIP"
          alias: "SourceIP"

```

###  Example
In this rule, you can define their whitelist of IPs. As an example, you have the ips whitelist 163.225.184.79,92.22.1.40,19.144.24.179,37e4:dd49:a173:02f4:3164:1df0:8849:6ef9 which you can change to your list

## 4. Microsoft 365: Detected user activity that is not in the white list of allowed users

### YAML Configuration:
```yaml
- name: "Microsoft 365: Detected user activity that is not in the white list of allowed users"
  severity: "High"
  description: "This alert is generated when a user is detected that is not on the white list of allowed users."
  solution: "We recommend carefully reviewing the logs to verify users who are not whitelisted."
  category: "Connection from non-whitelisted"
  tactic: ""
  dataTypes: ["o365"]
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - allOf: 
        - field: "logx.o365.UserId"
          operator: "not in"
          value: "cafroixeunnouxe-7608@yopmail.com,bineppohuno-6676@yopmail.com,keven_mohr@gmail.com"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.o365.UserId"
          alias: "SourceUser"
        - field: "logx.o365.ClientIP"
          alias: "SourceIP"

```
###  Example
In this rule, you can define your whitelist of users who can have activity. As an example, you have the whitelist of users cafroixeunnouxe-7608@yopmail.com,bineppohuno-6676@yopmail.com,keven_mohr@gmail.com which you can change to your list

## 5. Windows: Detected user activity that is not in the white list of allowed users

### YAML Configuration:
```yaml
- name: "Windows: Detected user activity that is not in the white list of allowed users"
  severity: "High"
  description: "This alert is generated when a user is detected that is not on the white list of allowed users."
  solution: "We recommend carefully reviewing the logs to verify users who are not whitelisted."
  category: "Connection from non-whitelisted"
  tactic: ""
  dataTypes: ["wineventlog"]
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - allOf:
        - field: "logx.wineventlog.event_data.SubjectUserName"
          operator: "not in"
          value: "cafroixeunnouxe-7608@yopmail.com,bineppohuno-6676@yopmail.com,keven_mohr@gmail.com"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.wineventlog.event_data.SubjectUserName"
          alias: "SourceUser"
        - field: "logx.wineventlog.host.name"
          alias: "DestinationHost"
        - field: "logx.wineventlog.event_data.IpAddress"
          alias: "DestinationIP"
        - field: "logx.wineventlog.event_data.IpPort"
          alias: "DestinationPort"
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
```
###  Example
In this rule, you can define your whitelist of users who can have activity. As an example, you have the whitelist of users cafroixeunnouxe-7608@yopmail.com,bineppohuno-6676@yopmail.com,keven_mohr@gmail.com which you can change to your list