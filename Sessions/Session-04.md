# Session 04 — Customizing Sysmon Network Monitoring

**Date:** 22 July 2026

---

# Objective

Customize the Sysmon configuration to monitor PowerShell network connections and validate that the new monitoring rule generates Event ID 3 successfully.

---

# Overview

This session focused on extending the default Sysmon monitoring capabilities by modifying the active configuration file.

A new NetworkConnect rule was added to monitor PowerShell outbound network activity. After reloading the configuration, validation testing confirmed that PowerShell network connections were successfully recorded as Event ID 3.

---

# Lab Activities

## Configuration Backup

- Created a backup of the original Sysmon configuration.
- Preserved the original configuration before making changes.

---

## Configuration Review

Reviewed the **NetworkConnect** include rules within the SwiftOnSecurity Sysmon configuration.

Identified that PowerShell network activity was not included by default.

---

## Rule Modification

Added a new **PowerShell.exe** rule to the NetworkConnect include section.

Saved the modified configuration.

---

## Reloading Sysmon

Reloaded the updated Sysmon configuration without reinstalling Sysmon.

Verified that the configuration loaded successfully.

---

## Validation

Generated outbound network activity using PowerShell.

Confirmed that Sysmon successfully generated **Event ID 3**.

Collected the following evidence:

- Image
- User
- Protocol
- Destination IP
- Destination Port
- Initiated

---

# Screenshots

- Screenshot 01 — Original NetworkConnect Rules
- Screenshot 02 — Modified PowerShell Rule
- Screenshot 03 — Reload Sysmon Configuration
- Screenshot 04 — Event ID 3 (PowerShell Network Connection)

---

# Skills Practiced

- Sysmon Configuration
- Network Monitoring
- Event ID 3 Investigation
- PowerShell
- Configuration Validation
- SOC Monitoring

---

# Lessons Learned

- Sysmon behavior is completely controlled by its configuration.
- Configuration changes can be applied without reinstalling Sysmon.
- Validation testing is required after every configuration update.
- Event ID 3 provides valuable visibility into outbound process communication.
- Building custom detection rules improves endpoint visibility.

---

# Session Outcome

✅ Successfully modified the Sysmon configuration.

✅ Added PowerShell network monitoring.

✅ Reloaded the configuration successfully.

✅ Validated PowerShell Event ID 3 generation.

The SOC lab now monitors outbound PowerShell network activity as part of endpoint telemetry.

---

# Next Session

- Investigate Event ID 11 (File Create).
- Generate file creation events.
- Understand how attackers create or drop files.
- Build the first structured SOC investigation report.