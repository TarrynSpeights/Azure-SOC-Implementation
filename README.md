# Azure SOC Implementation

## Overview

This project demonstrates the deployment of Microsoft Sentinel in Azure to collect and analyze Windows security events.

## Technologies Used

- Microsoft Azure
- Microsoft Sentinel
- Log Analytics Workspace
- Windows 10
- Kusto Query Language (KQL)

## What I Did

- Created an Azure Windows 10 virtual machine.
- Connected the VM to Microsoft Sentinel.
- Collected Windows security logs.
- Generated failed login attempts.
- Used a KQL query to detect Event ID 4625.

## Sample KQL Query

SecurityEvent
| where EventID == 4625
| project TimeGenerated, Computer, Account, IpAddress
| order by TimeGenerated desc
