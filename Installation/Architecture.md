---
layout: default
title: Architecture
parent: Installation
nav_order: 1
---


# Architecture and Deployment Models

UTMStack offers a flexible and scalable architecture, empowering organizations to choose from various deployment models that best suit their needs. Whether deployed on the cloud or on-premises, UTMStack can seamlessly adapt to any scenario, providing a robust and comprehensive cybersecurity solution.

# Deployment Models
UTMStack presents four compelling deployment models, each catering to specific requirements and offering distinct advantages:

## 1. Master Only Deployment: Unparalleled Data Control and Security

<img title="Master Only Diagram" alt="Master Only Diagram" src="../Images/Architecture/Master%20Only/diagram.png">

A **Master Only Deployment** of UTMStack is dedicated to an individual customer, ensuring unparalleled data control and security.

By opting for a master-only installation, organizations can maintain complete control over their data. UTMStack can be effortlessly deployed within the customer's network, whether on a virtual machine or a physical server. This approach allows for direct log gathering from customer devices and applications, ensuring data remains within the organization's boundaries.

With data isolation and enhanced security, the master-only deployment model offers peace of mind, particularly for organizations concerned about sharing sensitive information with third parties.

## 2. Federated Master Deployment: Streamlined Management for MSPs

<img title="Master Only Diagram" alt="Master Only Diagram" src="../Images/Architecture/Federated/diagram.png">

The **federated master deployment model** is ideal for Managed Service Providers (MSPs) managing multiple instances of UTMStack.

In this model, multiple master servers are deployed, with one in each customer's network. A central federation service acts as a unified monitoring panel, allowing MSPs to effortlessly oversee alerts generated by separate systems from a single centralized interface.

This streamlined approach simplifies monitoring and management, enabling MSPs to efficiently navigate activities across multiple clients and organizations. 

The federated master deployment model is commonly used by SOC teams for its simplicity and effectiveness.

## 3. SaaS (Software as a Service): Simplified Management with Unparalleled Support

<img title="Master Only Diagram" alt="Master Only Diagram" src="../Images/Architecture/SaaS/diagram.png">

For organizations seeking for a hassle-free and fully managed solution, UTMStack offers the **Software as a Service (SaaS) deployment model**.

With SaaS, organizations can benefit from a comprehensive managed instance of UTMStack, including updates, scaling, backups, high availability, and dedicated support. Logs can be effortlessly collected from customer systems by installing agents or configuring SyslogTLS or proxy.

This streamlined approach allows organizations to focus on their core business, leaving the complexities of cybersecurity management to the experts at UTMStack. Enjoy the peace of mind that comes with a fully managed solution, ensuring top-notch security and efficiency without the burden of infrastructure management.

UTMStack's flexible deployment models empower organizations and MSPs to choose the most suitable approach based on their specific requirements, infrastructure, and security preferences. By offering a range of options, UTMStack ensures that organizations of all sizes and complexities can enjoy the benefits of a robust and comprehensive cybersecurity platform.