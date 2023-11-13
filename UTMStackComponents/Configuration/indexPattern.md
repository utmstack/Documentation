---
layout: default
title: Index Patterns Management
parent: Configuration
nav_order: 7
---

# Index Patterns Management

- **Pattern**: This column lists the pattern used to match against multiple index names.
- **Used by Integration**: Indicates the integration from which the logs are generated.
- **Action**: Allows the user to perform actions such as editing or deleting the index patterns (only when it's not been used for the integration).

Examples of patterns and their uses:

- `log-*` - Matches all indices that start with `log-`.
- `alert-*` - Matches all indices that start with `alert-`.
- `log-winventlog-*` - Used for indices related to Windows event logs.
- `log-o365-*` - Used for Office 365 logs.
- `log-firewall-*` - Matches indices for various firewall logs.

The user can also create new index patterns to match their indexing needs by using the "Create index pattern" button.

This interface simplifies the process of managing which indices are analyzed and visualized in the system.