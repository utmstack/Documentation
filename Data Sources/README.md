---
layout: default
title: Data Sources
nav_order: 7
has_children: true
---

# Data Sources in UTMStack

The **Data Sources** section in UTMStack allows managing and monitoring data origins from various devices, cloud services, and agents. These sources provide logs and security events for analysis and threat detection. The interface includes the following features:

## Filters
- **Group**: Filter sources by assigned group.
- **Type**: Filter by source type (e.g., `generic`, `wineventlog`, `linux`).
- **Search in values**: Search sources by name or IP address.

## Sources Table
The table displays detailed information for each data source:
- **Status**: Indicates connection status:
  - `All connected`: All sources are connected.
  - `Connected`: Source is active and sending data.
  - `Disconnected`: Source is offline or not sending data.
- **Source**: Name or IP address of the origin.
- **Types**: Type of data source:
  - `generic`: General data origin.
  - `wineventlog`: Windows event log source.
  - `linux`: Linux log source.
- **Last Input**: Date and time of the last received input.
- **Action**: Manage each source:
  - **Delete** (`X`): Remove the source.
  - **View Details** (`screen icon`): This option is **only available for agents**, showing detailed information about the agent's configuration and status.

## Actions and Management
- **Manage source view**: Customize the table view.
- **Manage groups**: Organize sources into custom groups.
- **Add device**: Add new data sources to the system.
- **Search by source**: Quick search by name or IP address.

## Pagination and Display
- **Items per page**: Control the number of visible sources per page.
- Page navigation to access all registered sources.

## Usage Example
In the example shown:
- Data origins are monitored with different statuses (`Connected`, `Disconnected`).
- Sources of type `generic`, `wineventlog`, and `linux` are used.
- Last input is displayed for each source, helping identify inactive sources.

## Automatic Hostname and Preferred IP Selection

### Feature Description
In UTMStack, **agents** now have the capability to automatically update the **hostname** when the machine name changes. Additionally, users can **select a preferred IP address** for the agent, which will be used in visualizations and data entries.

### How It Works
1. **Hostname Update**:
   - When the machine's name is changed, the agent automatically detects the change and updates the **hostname** in the host list without manual intervention.
   - This change is immediately reflected in the **sources table**.

2. **Preferred IP Selection**:
   - In the agent detail screen, a list of **IP addresses** available on the machine is displayed.
   - Users can **select the preferred IP** from the list.
   - The selected IP becomes the **primary IP** used in dashboards and data entries.
     - This feature is designed to **prioritize the selected IP** for monitoring purposes without changing the device's actual IP settings.
     - It ensures accurate representation in visualizations and logs.

<img title="Collectors" alt="Collectors" src="../Images/selectip.png">

### Result

<img title="Collectors" alt="Collectors" src="../Images/selectipchanges.png">

### Important Notes
- This feature **does not** modify the network configuration of the device.
- The **preferred IP** is only used for **monitoring and visualization** within UTMStack.
- **View Details** is only available for agents, and the preferred IP selection can only be configured from this screen.

### Benefits
- **Automation**: No need for manual updates of hostname or IP.
- **Accurate Monitoring**: The selected IP ensures accurate data representation.
- **Efficiency**: Reduces human errors by automating the update process.

This section allows efficient management of data sources for continuous and effective security monitoring.