# Session 01 — Windows SOC Lab Setup

**Date:** 20 July 2026

---

# Objective

Build the Windows SOC Lab from scratch and prepare a Windows endpoint for future SOC monitoring and investigations.

---

# Overview

This session focused on building the foundation of the SOC lab by creating a dedicated Windows 11 virtual machine, preparing the operating system, and establishing a clean baseline before installing any security monitoring tools.

Creating a stable and repeatable environment is an essential first step before deploying Sysmon, collecting endpoint telemetry, and performing threat hunting activities.

---

# Lab Environment

| Component | Configuration |
|----------|---------------|
| Operating System | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Endpoint Name | SOC-WIN11-01 |
| Administrator Account | SOCAdmin |
| RAM | 6144 MB |
| CPU | 4 Cores |
| Disk | 80 GB |

---

# Tasks Completed

- Selected the host machine.
- Verified hardware specifications.
- Verified VirtualBox installation.
- Created the Windows SOC Lab project structure.
- Downloaded the Windows 11 ISO.
- Created the Windows 11 virtual machine (SOC-WIN11).
- Allocated hardware resources:
  - 6144 MB RAM
  - 4 CPU Cores
  - 80 GB Virtual Disk
- Installed Windows 11.
- Renamed the endpoint to **SOC-WIN11-01**.
- Created the **SOCAdmin** local administrator account.
- Installed VirtualBox Guest Additions.
- Created the initial VirtualBox snapshot (**Clean Windows 11**).

---

# Why This Matters

A clean baseline is essential for every SOC lab.

Without a known-good starting point, it becomes difficult to distinguish between legitimate operating system activity and suspicious behavior generated during investigations.

Creating snapshots also allows the analyst to quickly restore the environment before testing new attack scenarios.

---

# Skills Practiced

- Windows Deployment
- Virtual Machine Management
- VirtualBox Configuration
- Windows Endpoint Preparation
- Lab Planning
- Baseline Creation

---

# Lessons Learned

- A well-organized lab simplifies future investigations.
- Creating snapshots before major changes saves significant recovery time.
- Consistent endpoint naming improves investigation clarity.
- Building the environment correctly is just as important as performing investigations later.

---

# Session Outcome

✅ Windows 11 virtual machine deployed successfully.

✅ SOC endpoint configured.

✅ Clean baseline established.

✅ Initial recovery snapshot created.

The lab is now ready for endpoint monitoring and security tooling.

---

# Next Session

The next session focuses on deploying Sysmon, applying a professional configuration, and validating endpoint telemetry using Windows Event Viewer.