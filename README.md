# 🛡️ Splunk Detection Home Lab

## Project Overview
This repository contains configuration files, dashboards, and **Search Processing Language (SPL)** queries used to build a foundational security monitoring and threat detection capability using **Splunk Enterprise (Free)**.

The lab is primarily focused on **Windows logging** and event data analysis (e.g., Sysmon, Windows Security Logs).

## 🛠️ Environment Stack
* **SIEM:** Splunk Enterprise (Free License)
* **Endpoint:** Windows 10/11 (Alpha Laptop)
* **Data Ingestion:** Splunk Universal Forwarder
* **Detection Content:** Custom SPL, imported Sigma rules (when applicable).

## 🚀 Key Content & Detection Goals
### Log Ingestion
* **inputs.conf:** Configuration for ingesting Windows Event Logs (Security, Application, System).
* **Data Sources:** Focus on **Event Code 4688** (Process Creation) and **4624/4625** (Logons).

### Detection Examples
* **Initial Focus:** Detection of **brute force** attempts, **user privilege escalation**, and common **PowerShell abuse** techniques.
* *Example SPL:* `index=winlogs sourcetype=WinEventLog:Security EventCode=4625 | stats count by Logon_Type, IpAddress | where count > 5`

---
