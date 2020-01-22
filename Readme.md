# Log Analytics Queries
## Introduction
This repository contains Kusto queries that I wrote to support my own curiousity or that of my customers. For me, these scripts are a means to a goal - they are guaranteed to deviate from the recommended practices on writing performant or maintainable queries. You should consider them in that context. 

## Query 1: Platform Health
The [Queries/PlatformHealth.csl] script uses the Heartbeat and Activity logs to report on server availability, differentiating between user-initiated downtime (e.g. admins that deallocate or resize the machine) and platform-initiated downtime.

It requires a Log Analytics workspace that actually collects the Heartbeat data and [Activity Log](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/activity-log-collect), so make sure you collect that information if the report doesn't give you results.