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
| User           | `cyberlab`                      |
| Host           | `DESKTOP-96GH4UH`                         |
| Timestamp      | `Aug 22, 2026 @ 12:20:33.242`                        |
| Command line   | `"powershell.exe" -NoProfile -WindowStyle Hidden -Command "Write-Output 'SOC lab simulation'"`            |
| Parent process | `powershell.exe`          |

## Evidence Screenshot

### PowerShell Process Creation — Sysmon Event ID 1

<img width="1873" height="229" alt="Wazuh-powershell" src="https://github.com/user-attachments/assets/a57310b4-5f3e-4c84-b96e-c414b14e7af0" />

<img width="936" height="813" alt="Wazuh-powershell-process-detail" src="https://github.com/user-attachments/assets/9328bf42-32d9-4020-be9e-1dd04e1462d1" />



## Assessment

PowerShell was executed with command-line arguments that were considered suspicious in the context of the alert.

The PowerShell execution contained command-line characteristics that can warrant investigation, including `-NoProfile` and `-WindowStyle` Hidden. The available telemetry was sufficient to demonstrate how an L1 analyst would assess and escalate a suspicious PowerShell alert. The command was intentionally generated as part of the controlled lab simulation. Further investigation is required to determine the purpose of the command and whether the execution was authorized.

## Disposition

**Escalate to L2**

### Recommended L2 Actions

* Determine whether the PowerShell execution was authorized.
* Analyse the command and its intended behaviour.
* Review related process and child-process activity.
* Review relevant network activity.
* Determine whether additional endpoint investigation is required.

**Lab note:** The PowerShell command used in this project was intentionally designed to be harmless while generating telemetry for a controlled SOC investigation.
