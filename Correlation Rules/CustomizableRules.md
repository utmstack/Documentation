---
layout: default
title: Customizable Rules
parent: Correlation Rules
nav_order: 3
---

# Customizable Rules

UTMStack allows users to define customizable rules to enhance the monitoring and alerting based on specific requirements of their network environments. Below are a few examples of such customizable rules, each tailored for different use-cases:

## Rule 1: Whitelist of Internal IPs
Users can define a whitelist of internal IPs that are considered safe. Any activity detected from IPs not in this whitelist will trigger an alert.

### YAML Configuration:
```yaml
- name: "Windows: Activity detected from non-whitelisted internal IPs"
  severity: "High"
  description: "Activity has been detected from an IP that is not on the whitelist of allowed internal IPs"
  solution: "We recommend carefully reviewing the logs to verify activity from an IP that is not on the whitelist of allowed internal IPs"
  category: "Connection from non-whitelisted"
  tactic: ""
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
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
        - field: "logx.wineventlog.host.name"
          alias: "SourceHost"
```

###  Example
In this rule, an alert is generated if there is any activity detected from IPs not listed in the whitelist 10.0.2.27,192.168.22.128,fe80::97d1:5df4:10fe:7b8d.

## Rule 2: Whitelist of Allowed Applications
Users can define a whitelist of applications that are permitted to run on the servers. Any activity detected from applications not in this whitelist will trigger an alert.

### YAML Configuration:
``` yml
- name: "Windows: Detected application that is not in the white list of allowed applications"
  severity: "High"
  description: "This alert is generated when an application that is not on the white list of allowed applications is detected."
  solution: "We recommend carefully reviewing the logs to verify applications that are not whitelisted"
  category: "Connection from non-whitelisted"
  tactic: ""
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
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
        - field: "logx.wineventlog.host.name"
          alias: "SourceHost"
```

### Example
In this rule, an alert is generated if any application other than svchost.exe, services.exe, or poqexec.exe is detected running on the servers.

## Rule 3: Whitelist of IPs for Microsoft 365 Logins

Users can define a whitelist of IPs from which logins to Microsoft 365 are allowed. Any login attempts from IPs not in this whitelist will trigger an alert.

### YAML Configuration:

``` yml
- name: "Microsoft 365: Login detected from non-whitelisted IP"
  severity: "High"
  description: "A user is trying to login from an IP that is not on the whitelist"
  solution: "We recommend carefully reviewing the logs to verify users attempting to login from an IP that is not on the whitelist"
  category: "Connection from non-whitelisted"
  tactic: ""
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

### Example
In this rule, an alert is generated if a user tries to login to Microsoft 365 from any IP other than 163.225.184.79, 92.22.1.40, 19.144.24.179, 37e4:dd49:a173:02f4:3164:1df0:8849:6ef9.


## Rule 4: Whitelist of Allowed Users for Microsoft 365 Activity

Users can define a whitelist of user accounts that are allowed to have activity in Microsoft 365. Any activity from user accounts not in this whitelist will trigger an alert.

### YAML Configuration:

``` yml
- name: "Microsoft 365: Activity detected from non-whitelisted user"
  severity: "High"
  description: "Activity has been detected from a user that is not on the whitelist"
  solution: "We recommend carefully reviewing the logs to verify activity from a user that is not on the whitelist"
  category: "Connection from non-whitelisted"
  tactic: ""
  reference: 
    - "https://en.wikipedia.org/wiki/Whitelist"
  frequency: 60
  cache:
    - allOf:
        - field: "logx.o365.UserId"
          operator: "not in"
          value: "john.doe@example.com,jane.doe@example.com"
        - field: "logx.o365.ResultStatus"
          operator: "in"
          value: "Success,PartiallySucceeded,True"
      minCount: 1
      timeLapse: 60
      save:
        - field: "logx.o365.UserId"
          alias: "SourceUser"
```

### Example:
In this rule, an alert is generated if any activity is detected from user accounts other than john.doe@example.com or jane.doe@example.com in Microsoft 365.

## Rule 5: Windows User Activity Outside Whitelist Detected

In this rule, you can define a whitelist of users who are authorized to carry out activities on the Windows environment. For instance, the whitelist of users is specified as cafroixeunnouxe-7608@yopmail.com, bineppohuno-6676@yopmail.com, and keven_mohr@gmail.com, which can be tailored to match your list of authorized users. Users should be delineated by commas.

### YAML Configuration:

``` yml
- name: "Windows: Detected user activity that is not in the white list of allowed users"
  severity: "High"
  description: "This alert is generated when a user is detected that is not on the white list of allowed users."
  solution: "We recommend carefully reviewing the logs to verify users who are not whitelisted."
  category: "Connection from non-whitelisted"
  tactic: ""
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
        - field: "logx.wineventlog.event_data.TargetUserName"
          alias: "DestinationUser"
        - field: "logx.wineventlog.host.name"
          alias: "SourceHost"

```

### Example:
In this rule configuration, an alert is triggered whenever user activity is detected from accounts other than those listed in the whitelist: cafroixeunnouxe-7608@yopmail.com, bineppohuno-6676@yopmail.com, and keven_mohr@gmail.com. The aim is to promptly identify and respond to potential unauthorized access or malicious activities by unlisted users within the Windows environment.