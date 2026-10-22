This repository contains Scanner detection rules for Windows PowerShell logs. Rule filenames use a two-part
prefix — `posh_` for PowerShell, followed by `pc`, `pm`, or `ps` to indicate the log source (classic channel,
module logging, or script block logging).

## Examples

Here are a few examples of the detections that are included in this repository:

* AADInternals PowerShell Cmdlets Execution - PsScript
* HackTool - Rubeus Execution - ScriptBlock
* Invoke-Obfuscation Obfuscated IEX Invocation - PowerShell


## Event Sinks

When these detection rules are triggered, alerts are sent to the [event sinks](https://docs.scanner.dev/scanner/using-scanner-complete-feature-reference/detections-and-alerting/event-sinks) you have configured in Scanner. Depending on the alert's severity level, it will be sent to one of these event sink keys:

* `informational_severity_alerts`
* `low_severity_alerts`
* `medium_severity_alerts`
* `high_severity_alerts`
* `critical_severity_alerts`
* `fatal_severity_alerts`

## Deployment

To deploy these rules into your Scanner instance, you can follow the instructions in the
[Scanner documentation](https://docs.scanner.dev/) under Detection Rules as Code.
