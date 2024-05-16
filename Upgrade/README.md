---
layout: default
title: Update
nav_order: 5
has_children: true
---

# UTMStack Update Guide

Keeping your UTMSTACK software up to date is essential for maintaining system security, performance, and access to the latest features. This guide will walk you through the necessary steps to update UTMSTACK to the latest version.

1. Update packages list:

```bash
sudo apt update
```

2. Download the latest version of the installer:

```bash
wget http://github.com/utmstack/UTMStack/releases/latest/download/installer
```

3. Change to root user:

```bash
sudo su
```

4. Set execution permissions:

```bash
chmod +x installer
```

5. Execute the installer:

```bash
./installer
```