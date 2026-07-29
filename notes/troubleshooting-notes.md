# Troubleshooting Notes

## Issue 1

Unable to create folders using environment variables.

### Cause

PowerShell session was not running from the expected user context.

### Resolution

Navigate to the user profile first:

```powershell
cd C:\Users\<Username>
```

---

## Issue 2

Environment variable returned unexpected path.

### Cause

Incorrect environment variable used.

### Resolution

Verify the current profile:

```powershell
Get-ChildItem "$env:USERPROFILE"
```

---

## Issue 3

Desktop folder not found.

### Cause

Incorrect folder path.

### Resolution

Confirm Desktop exists:

```powershell
Get-ChildItem "$env:USERPROFILE\Desktop"
```

---

## Issue 4

Downloads folder not found.

### Cause

Incorrect path or typo.

### Resolution

Verify Downloads folder:

```powershell
Get-ChildItem "$env:USERPROFILE\Downloads"
```

---

## Issue 5

Recently modified files did not include newly created artifacts.

### Cause

Files were created after running the enumeration command.

### Resolution

Run the command again:

```powershell
Get-ChildItem "$env:USERPROFILE" -Recurse |
Sort-Object LastWriteTime -Descending |
Select-Object -First 15 Name, FullName, LastWriteTime
```

---

## Issue 6

Cleanup failed.

### Cause

Incorrect folder path or folder already removed.

### Resolution

Verify the folder exists before deletion:

```powershell
Get-ChildItem "$env:USERPROFILE\Desktop"
Get-ChildItem "$env:USERPROFILE\Downloads"
```

Then remove the remaining lab artifacts.
