---
layout: default
title: FAQs
nav_order: 18
---

## Frequently Asked Questions (FAQ)

## FAQs for Documentation (English Version)

1. **What should we do if the master server's hard disk becomes full?**  
   We recommend using a disk with a minimum capacity of 1 TB for data storage. This recommendation aligns with the platform's backup retention policies, typically set to one year.

2. **How can we back up the master server logs to backup storage?**  
   Map an NFS server disk to the `/utmstack/opensearch/backups` folder. This method ensures secure and efficient storage of master server logs in the designated backup location.

3. **How long are logs retained, and are they deleted automatically?**  
   Logs are retained based on the client's policy. After this period, they are archived in the `/utmstack/opensearch/backups` folder. Typically, logs are kept for one year.

4. **Should we be concerned about application log errors?**  
   These logs are internal system messages and generally do not require attention.

5. **How can we create a menu?**  
   Follow the instructions provided in [Dashboard](https://docs.utmstack.com/UTMStackComponents/Dashboards/README.html)

6. **Can we forward logs from UTMStack to another SIEM?**  
   No, UTMStack does not support forwarding logs to other SIEM platforms.

7. **How do we integrate third-party applications?**  
   UTMStack supports multiple log sources and allows the receipt of non-integrated app logs via Syslog and HTTP Post.

8. **Can we install the Windows Agent on Windows Server 2008?**  
   No, the Windows Agent is compatible with Windows Server 2012R2 or higher. Alternatively, use NXLog to send logs via Syslog.

9. **Do you offer older versions of the current agent?**  
   No, older versions are not compatible with UTMStack V10.

10. **How do we change the time zone settings on the federal server?**  
    Go to **Settings > Application Settings** via the right-side hamburger menu, where you will find the option to change the platform’s time zone.

11. **How can we generate reports of processed and closed incidents?**  
    Create a custom dashboard with the relevant data and export it as a PDF. You can also set up an automated schedule for email delivery.

12. **How can I block an IP address using a command?**  
   After identifying the command to block the IP address, you can use a variable from the alert to pass the IP to the command. For example:
   ```bash
   $ ssh -o StrictHostKeyChecking=accept-new -i /root/.ssh/id_rsa admin@192.168.1.1 command-to-block-ip $(source.ip)
   ```
13. **How are commands executed on remote hosts using UTMStack?**
    The incident response automation is designed to execute commands on Linux and Windows systems via SSH. For example:
    ```bash
    $ ssh -o StrictHostKeyChecking=accept-new admin@192.168.1.1 -i /root/.ssh/id_rsa echo hello
    ```
    SSH will connect to the host 192.168.1.1 using admin, authenticate with the SSH key, and execute the command.

14. **Do you provide third-party vendor support?**
    No, we do not provide third-party vendor support. Refer to the vendor documentation for specific commands.

15. **How can I get training on the incident automation feature?**
    Contact your account executive to schedule a session for in-depth training on the incident automation feature.