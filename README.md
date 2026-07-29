# windows-dfir-lab34-user-profile-tampering-investigation
## Overview

Windows user profiles contain valuable forensic artifacts that record a user's files, folders, and activity. During incident response, investigators frequently examine profile directories to identify unauthorized changes, suspicious files, or evidence of account misuse.

In this hands-on DFIR lab, a baseline Windows user profile was established before simulating suspicious activity through the creation of new folders and files. Native Windows tools and PowerShell were then used to identify recently modified artifacts and correlate profile changes with user activity.

---

# Executive Summary

This investigation demonstrates how Windows user profiles can be analyzed for evidence of suspicious modifications without relying on third-party forensic software. By comparing baseline profile contents with newly introduced artifacts, the investigation identified recently modified files and directories that could indicate unauthorized user activity or malware staging.

The workflow mirrors a common DFIR approach of establishing a baseline, detecting changes, validating evidence, and documenting findings.

---

# Investigation Objectives

- Examine the Windows user profile structure.
- Establish a baseline of user profile contents.
- Simulate suspicious profile modifications.
- Detect newly created folders and files.
- Identify recently modified artifacts.
- Correlate evidence to reconstruct user activity.
- Document forensic findings.

---

# Skills Demonstrated

- Windows User Profile Analysis
- Windows DFIR Methodology
- Host-Based Forensic Investigation
- Baseline vs Change Analysis
- PowerShell Enumeration
- Windows File System Investigation
- Timestamp Analysis
- Evidence Correlation
- Documentation of Investigation Findings
- Incident Reporting

---

# Tools Used

- Windows 10
- PowerShell
- File Explorer

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 10 |
| Investigation Type | Host-Based DFIR |
| Analysis Method | Native Windows Tools |
| Primary Artifact | Windows User Profile |
| Shell | Windows PowerShell |
| Privileges | Administrator |

---

# Investigation Workflow

1. Create investigation workspace.
2. Examine baseline user profile.
3. Simulate profile modifications.
4. Enumerate Desktop and Downloads.
5. Identify recently modified artifacts.
6. Correlate profile changes.
7. Document findings.
8. Remove lab artifacts.

---

# MITRE ATT&CK Mapping

| Technique | Description |
|-----------|-------------|
| T1083 | File and Directory Discovery |
| T1005 | Data from Local System |
| T1070 | Indicator Removal on Host |
| T1547 | Boot or Logon Autostart Execution (Potential Follow-on Investigation) |

---

# Evidence Collected

- User profile directory listing
- Desktop artifact enumeration
- Downloads artifact enumeration
- Recently modified file listing
- PowerShell outputs
- Folder creation evidence
- File creation timestamps

---

# Evidence Correlation

The investigation correlated multiple host artifacts to validate profile modifications:

- Baseline profile contents were compared against post-modification results.
- Newly created folders were confirmed through PowerShell enumeration.
- Recently modified files aligned with simulated activity timestamps.
- Desktop and Downloads artifacts were successfully correlated with user actions performed during the lab.

---

# Investigation Findings

The investigation confirmed that Windows user profiles preserve valuable evidence of user activity. Newly created folders and files were successfully identified, while PowerShell enumeration provided a reliable method for detecting recent modifications. Comparing baseline profile contents with current artifacts enabled rapid identification of suspicious changes without requiring specialized forensic software.

---


# Key Takeaway

Windows user profiles provide a rich source of forensic evidence for incident responders. Establishing a baseline and identifying deviations allows analysts to quickly detect unauthorized changes, reconstruct user activity, and prioritize areas for deeper forensic analysis.
