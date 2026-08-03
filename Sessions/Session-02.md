# Session 02 — Sysmon Deployment and Initial Telemetry

**Date:** 20–21 July 2026

---

# Objective

Deploy Microsoft Sysmon, apply a professional configuration, and validate endpoint telemetry collection using Windows Event Viewer.

---

# Overview

In this session, Sysmon was installed to extend the default Windows logging capabilities and provide detailed endpoint telemetry required for Security Operations Center (SOC) investigations.

A production-grade Sysmon configuration from SwiftOnSecurity was applied to improve event visibility while reducing unnecessary logging noise.

---

# Lab Activities

## Sysmon Installation

- Downloaded Microsoft Sysinternals Sysmon.
- Extracted the Sysmon package.
- Created the following directory:

```
C:\Tools\Sysmon
```

- Copied the following files:
  - Sysmon64.exe
  - Sysmon.exe

---

## Configuration

- Downloaded the SwiftOnSecurity Sysmon configuration.
- Saved the configuration inside:

```
C:\Tools\Sysmon
```

- Installed Sysmon using the configuration file.
- Reloaded and verified the configuration successfully.

---

## Validation

Opened:

```
Event Viewer
→ Applications and Services Logs
→ Microsoft
→ Windows
→ Sysmon
→ Operational
```

Verified that Sysmon was generating telemetry correctly.

Generated the first **Process Create (Event ID 1)** event.

Collected the following fields:

- Image
- CommandLine
- ParentImage
- User

---

# Screenshots

- Screenshot 01 — Sysmon Files
- Screenshot 02 — Sysmon Installation
- Screenshot 03 — Sysmon Operational Log
- Screenshot 04 — Event ID 1 (Process Create)

---

# Skills Practiced

- Sysmon Installation
- Endpoint Monitoring
- Windows Event Viewer
- Process Monitoring
- Endpoint Telemetry Collection
- SOC Lab Configuration

---

# Lessons Learned

- Sysmon significantly extends Windows Event Logging.
- Event ID 1 records every newly created process.
- Process metadata provides valuable investigation evidence.
- A well-designed Sysmon configuration improves visibility while reducing unnecessary events.
- Proper endpoint telemetry is the foundation of effective threat hunting.

---

# Session Outcome

✅ Sysmon successfully installed.

✅ Professional configuration applied.

✅ Operational logs verified.

✅ Event ID 1 successfully generated and analyzed.

The Windows endpoint is now capable of producing detailed telemetry for future investigations.

---

# Next Session

- Investigate Event ID 3 (Network Connection).
- Analyze outbound network activity.
- Understand how Sysmon NetworkConnect rules control telemetry collection.