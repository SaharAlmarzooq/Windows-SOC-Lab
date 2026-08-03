# Session 05 — File Creation Monitoring (Event ID 11)

**Date:** 22 July 2026

---

# Objective

Investigate Sysmon File Create events (Event ID 11) to understand how Sysmon monitors file creation activity and how configuration rules determine which files are logged.

---

# Overview

This session focused on validating Sysmon Event ID 11 by generating file creation activity and understanding why some files are logged while others are ignored.

The investigation demonstrated that Sysmon only records file creation events that match the configured monitoring rules, highlighting the importance of reviewing and understanding the active configuration.

---

# Lab Activities

## Configuration Review

Reviewed the SwiftOnSecurity **FileCreate** configuration.

Identified the file extensions monitored by Sysmon.

Confirmed that **.txt** files were excluded from monitoring.

---

## File Creation Testing

Created a text file.

Verified that no Event ID 11 was generated.

Created a PowerShell script:

```
TestScript.ps1
```

Generated Event ID 11 successfully.

---

## Investigation

Reviewed Event ID 11 and collected:

- Image
- TargetFilename
- User

Verified that PowerShell created the monitored file successfully.

---

## Documentation

Created the first SOC Investigation Report in Markdown format.

Recorded all collected evidence and investigation findings.

---

# Screenshots

- Screenshot 01 — FileCreate Configuration
- Screenshot 02 — Create TestScript.ps1
- Screenshot 03 — Event ID 11 (File Create)

---

# Skills Practiced

- Event ID 11 Investigation
- File Monitoring
- Sysmon Configuration Analysis
- PowerShell
- Incident Documentation
- Evidence Collection

---

# Lessons Learned

- Event ID 11 records monitored file creation activity.
- Sysmon only records files that match its configuration.
- Understanding monitoring rules is essential before troubleshooting missing events.
- Reviewing configuration files helps explain telemetry behavior.
- Documentation is an important part of every SOC investigation.

---

# Session Outcome

✅ Successfully validated Event ID 11.

✅ Understood FileCreate monitoring behavior.

✅ Confirmed configuration-based logging.

✅ Created the first SOC investigation report.

The Windows SOC Lab now provides visibility into monitored file creation activity.

---

# Next Session

- Investigate Registry monitoring.
- Explore Event ID 13 (Registry Value Set).
- Learn how Registry persistence techniques are detected.