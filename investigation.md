# Suspicious PowerShell Execution

**Severity:** Medium

**Disposition:** Escalate to L2

**Tools:** Wazuh, Sysmon

## Alert

Wazuh generated an alert for suspicious PowerShell execution on a Windows endpoint.

## Evidence

| Indicator      | Finding                              |
| -------------- | ------------------------------------ |
| Process        | `powershell.exe`                     |
| Event          | Sysmon Event ID 1 — Process Creation |
| User           | `[lab account]`                      |
| Host           | `[hostname]`                         |
| Timestamp      | `[timestamp]`                        |
| Command line   | `[observed command line]`            |
| Parent process | `[observed parent process]`          |

## Evidence Screenshot

### PowerShell Process Creation — Sysmon Event ID 1

*[Insert Wazuh/Sysmon screenshot here]*

## Assessment

PowerShell was executed with command-line arguments that were considered suspicious in the context of the alert.

The available telemetry was sufficient to establish suspicious PowerShell activity. Further investigation is required to determine the purpose of the command and whether the execution was authorized.

## Disposition

**Escalate to L2**

### Recommended L2 Actions

* Determine whether the PowerShell execution was authorized.
* Analyse the command and its intended behaviour.
* Review related process and child-process activity.
* Review relevant network activity.
* Determine whether additional endpoint investigation is required.

**Lab note:** The PowerShell command used in this project was intentionally designed to be harmless while generating telemetry for a controlled SOC investigation.
