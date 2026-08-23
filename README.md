# 02_Suspicious-PowerShell

## Objective

Investigate a suspicious PowerShell execution detected on a Windows endpoint using Wazuh and Sysmon.

## Environment

- Windows endpoint
- Wazuh
- Sysmon
- Controlled lab environment

## Scenario

A suspicious PowerShell execution was detected on a Windows endpoint.

The alert was reviewed to determine what PowerShell command was executed, which user initiated it, and whether the activity appeared suspicious.

## Investigation Flow

1. Review the Wazuh alert
2. Review the PowerShell command line
3. Identify the user and endpoint
4. Review the parent process
5. Assess whether the activity appears legitimate or suspicious
6. Determine the appropriate L1 disposition
7. Escalate to L2 if further investigation is required

## Key Evidence

- Wazuh PowerShell alert
- Sysmon Event ID 1 — Process Creation
- PowerShell command line
- User and endpoint information
- Timestamp

## Outcome

- **Finding:** Suspicious PowerShell execution
- **Disposition:** Escalated to L2
- **Key evidence:** PowerShell execution with suspicious characteristics requiring further investigation

## Report

[View the investigation report](investigation-report.md)

## Medium Post

[View the investigation in detail](https://medium.com/@larry.kaheiwong/investigating-a-suspicious-powershell-alert-with-wazuh-and-sysmon-53dbfe059402)
