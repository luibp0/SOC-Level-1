# Splunk: The Basics

## Overview

This room introduces the fundamentals of Splunk and how it can be used by SOC analysts to collect, search, analyze, and visualize security data.
It also provides practical experience with log ingestion and basic SPL queries.

## Topics Covered

- Splunk Fundamentals
- Splunk Architecture
- Data Ingestion
- Indexes
- Sources and Source Types
- Search Processing Language (SPL)
- Fields and Filters
- Search & Reporting
- Visualizations
- Dashboards

## Splunk Components

Splunk consists of several core components:

- **Forwarder:** Collects logs from different endpoints and sends them to Splunk.
- **Indexer:** Processes and stores incoming data so it can be searched.
- **Search Head:** Provides the interface used to search and analyze data using SPL.

## Data Ingestion

The basic process of adding data to Splunk includes:

- Selecting the data source
- Choosing the appropriate source type
- Selecting or creating an index
- Configuring the host information
- Reviewing and submitting the data

## Search Processing Language (SPL)

SPL is the language used to search and analyze data in Splunk.

Example:

```spl
index=vpn_logs
```

This query searches for events stored in the `vpn_logs` index.

SPL can be used to:

- Search and filter events
- Analyze specific fields
- Count and organize results
- Investigate suspicious activity
- Create reports and visualizations

## Practical Experience

During the practical exercises, I worked with:

- Uploading VPN logs
- Creating the `vpn_logs` index
- Searching indexed data
- Writing basic SPL queries
- Filtering events using fields
- Creating saved searches
- Building visualizations
- Creating dashboards

## Skills Learned

- Understanding basic Splunk architecture
- Ingesting and organizing log data
- Using indexes and source types
- Writing basic SPL queries
- Searching and filtering security events
- Creating visualizations and dashboards
- Using Splunk for basic SOC investigations

## Key Takeaway

Splunk helps SOC analysts collect, organize, search, and analyze security logs from different sources. Learning SPL and understanding how Splunk handles data are essential skills for investigating security events in a SOC environment.
