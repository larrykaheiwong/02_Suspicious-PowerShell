# 02_Suspicious-PowerShell# 03_PowerShell-Investigation

## Objective

Investigate a suspicious PowerShell execution detected on a Windows endpoint using Wazuh and Sysmon.

## Environment

* Windows endpoint
* Wazuh
* Sysmon
* Controlled lab environment

## Scenario

A suspicious PowerShell execution was detected on a Windows endpoint.

The alert was reviewed to determine what PowerShell command was executed, which user initiated it, and whether the activity appeared suspicious.

## Investigation Flow

1. Review the Wazuh alert
2. Review the PowerShell command line
3. Identify the user and endpoint
4. Review the parent process
5. Assess whether the activity is expected
6. Determine the appropriate L1 disposition
7. Escalate to L2 if further investigation is required

## Key Evidence

* Wazuh PowerShell alert
* Sysmon Event ID 1 — Process Creation
* PowerShell command line
* User and endpoint information
* Timestamp

## Disposition

**Suspicious — Escalate to L2**

## Report

[View the investigation report](investigation-report.md)
