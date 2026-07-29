# Investigation Notes

## Lab Summary

**Objective:**

Investigate a Windows user profile by establishing a baseline, simulating profile modifications, identifying recently modified artifacts, and correlating changes using native Windows tools.

---

## Analyst Methodology

The investigation followed a standard host-based DFIR methodology:

1. Establish baseline profile contents.
2. Simulate user profile modifications.
3. Enumerate Desktop and Downloads.
4. Identify newly created artifacts.
5. Analyze recently modified files.
6. Correlate profile evidence.
7. Document findings.
8. Perform cleanup.

---

## Investigation Steps

### Step 1

Created the investigation workspace.

**Evidence:**

- C:\UserProfileLab

---

### Step 2

Documented the baseline user profile.

Collected:

- Desktop
- Documents
- Downloads

---

### Step 3

Created simulated artifacts.

Evidence:

- ProjectFiles folder
- ClientList.xlsx
- Archive folder
- Passwords.txt

---

### Step 4

Enumerated Desktop.

Observation:

ProjectFiles directory and ClientList.xlsx were successfully identified.

---

### Step 5

Enumerated Downloads.

Observation:

Archive folder and Passwords.txt were identified.

---

### Step 6

Identified recently modified profile artifacts.

PowerShell sorted profile contents using LastWriteTime.

Observation:

Recently modified files appeared at the top of the results.

---

### Step 7

Correlated profile activity.

Compared:

- Baseline profile
- New folders
- New files
- Modification timestamps

Confirmed successful reconstruction of simulated user activity.

---

## Evidence Summary

Collected:

- PowerShell outputs
- Desktop enumeration
- Downloads enumeration
- Recently modified files
- Folder creation evidence
- Cleanup verification

---

## Analyst Observations

The investigation demonstrated that:

- Windows user profiles preserve valuable evidence of user activity.
- Recently modified artifacts can be rapidly identified using native PowerShell commands.
- Comparing baseline profile contents against current state provides an effective method for detecting suspicious modifications.
- Profile analysis supports incident response by highlighting newly created folders, files, and user activity.

---

## Conclusion

The investigation successfully demonstrated host-based Windows user profile analysis by establishing a baseline, identifying suspicious profile modifications, correlating newly created artifacts, and documenting evidence using native Windows utilities.
