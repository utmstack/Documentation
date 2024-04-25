---
layout: default
title: Application Settings
parent: Configuration
nav_order: 4
---

# APPLICATION SETTINGS

UTMStack offers a comprehensive configuration module where administrators can adjust various settings to customize the application according to their organizational preferences. Here's a detailed breakdown:

## Email Notifications

Configure the email settings to send emails notifications for the alerts and incidents:

- **Mail Server Password**: The password for your email server to authenticate and send out notifications.

- **UTMStack email address**: The official UTMStack email address that will be used to send out notifications.

- **UTMStack base url**: For example: `https://UTMStack.UTMStack.com`.

- **Mail Server Host**: For example: `example.hostmail.com`.

- **Mail Server Port**: Typically, the port can be `587`.

- **Mail Server Username**: The username for your email server.

- **Encryption type**: Choose the encryption protocol for your email server. Options include:
  - STARTTLS
  - SSL/TLS
  - NONE 



## Two Factor Authentication (2FA)

2FA is a security mechanism where users must provide two separate verification methods to access an account or application. This feature enhances the application's security:

- **Enable Two Factor Authentication**: Toggle this option to enable or disable 2FA for user access.


## Alerts Configuration

Define settings for alert and incident notifications:

- **Emails to notify incidents**: List down the email addresses that should receive incident notifications.

- **Emails to notify alerts**: Specify the email addresses that should receive alert notifications.

## Date Settings

Set your default time zone and date format preferences:

- **Time Zone**: Choose the time zone in which you want to view the logs. By default, logs are stored in UTC.

- **Date Format**: Choose your preferred date format, such as `Medium`.
