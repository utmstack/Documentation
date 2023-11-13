---
layout: default
title: Application Settings
parent: Configuration
nav_order: 4
---

# APPLICATION SETTINGS

UTMStack offers a comprehensive configuration module where administrators can adjust various settings to customize the application according to their organizational preferences. Here's a detailed breakdown:

## SMS Notifications using Twilio

UTMStack has integrated with Twilio, a renowned cloud communications platform, to facilitate SMS notifications. To ensure timely and accurate SMS delivery, it's crucial to configure the following parameters:

- **Twilio Authentication Token**: This secret token is used to authenticate your Twilio account. Ensure you enter the correct token to maintain seamless communication.
  
- **Twilio Account SID**: Your unique Twilio Account identifier. It's crucial for distinguishing and authorizing your Twilio account.

- **Twilio Virtual Phone Number**: This is the dedicated phone number from which SMS notifications will be sent. It must be procured from your Twilio dashboard.


## Email Notifications

Configure the email settings to send emails notifications for the alerts and incidents:

- **Mail Server Password**: The password for your email server to authenticate and send out notifications.

- **UTMStack email address**: The official UTMStack email address that will be used to send out notifications.

- **UTMStack base url**: For example: `https://UTMStack.UTMStack.com`.

- **Mail Server Host**: For example: `example.hostmail.com`.

- **Mail Server Port**: Typically, the port can be `587`.

- **Mail Server Username**: The username for your email server.

- **Encryption type**: Choose the encryption protocol for your email server. Options include:
  - TLS
  - SSL
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
