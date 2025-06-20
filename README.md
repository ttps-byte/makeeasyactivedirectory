# ACTIVEDIRECTORY POWERSHELL MODULE OVERVIEW

The `ActiveDirectory` PowerShell module provides a comprehensive set of cmdlets that assist in managing and querying an Active Directory environment via the command line. With over 140 cmdlets available, it enables both administrators and security professionals to retrieve critical directory information without the need for third-party tools.

This guide focuses on a subset of cmdlets commonly used during directory enumeration in authorized environments. For broader exploration, users are encouraged to consult the module documentation and experiment in lab setups.

## VERIFYING MODULE AVAILABILITY

Before using any of the Active Directory-specific commands, ensure that the module is available and properly loaded.

To list all currently imported modules:

```powershell
Get-Module
```
This will return a list of loaded modules, including their names, versions, and available commands.

If the ActiveDirectory module is not listed, load it using:

```Import-Module ActiveDirectory```

After loading, confirm it's active by running Get-Module again.

~~~~PS C:\> Get-Module

ModuleType Version    Name                 ExportedCommands
---------- -------    ----                 ----------------
Manifest   1.0.1.0    ActiveDirectory      {Add-ADComputerServiceAccount, Get-ADUser, Get-ADGroup, ...}
~~~~
