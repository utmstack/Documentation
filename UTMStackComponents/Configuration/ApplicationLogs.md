---
layout: default
title: Application Logs Overview
parent: Configuration
nav_order: 8
---

## Application Logs

The Application Logs provide a chronological record of events and errors within the system.

### Log Entries Structure

Each log entry consists of the following components:

- **Date**: The timestamp when the log entry was recorded.
- **Source**: The origin of the log entry. Ex: `PANEL`.
- **Type**: The nature of the log, which currently shows as `ERROR` for all entries.
- **Preview**: A brief snippet indicating the nature of the log entry, often containing the name of the method or operation that triggered the log entry.

### Frequent Errors and Possible Causes

The errors provided in the logs suggest a few possible recurring issues:

1. **Index Property Retrieval**: Repeated `ElasticsearchResource.getIndexProperties` errors may indicate problems accessing index configuration details.
2. **Index Existence Check**: Frequent `ElasticsearchService.indexExist` errors could signify attempts to access non-existent indices or issues with index creation.
3. **Cluster Status Issues**: The `ElasticsearchResource.getClusterStatus` error points towards potential issues with the Elasticsearch cluster health.
4. **Space Management**: The `ElasticsearchService.preventSystemCrashBySpace` log suggests there are automated measures to handle low disk space conditions.

### Recommended Actions

- **Analyze the Errors**: Review the error details to diagnose the underlying problems.
- **Resource Availability**: Confirm that the Elasticsearch cluster has sufficient resources and is configured correctly.
- **Space Management**: Monitor disk space and ensure there are appropriate measures to handle space-related issues.
- **Search for Patterns**: Look for timing patterns that might correlate with scheduled tasks or system load.
- **Review Changes**: Audit any recent changes to system configurations or deployments.
- **Monitoring and Alerts**: Implement or update monitoring and alerting strategies to proactively address these errors.

