# Windows 10 | Debloat

Tired of candy crush in your menu?

Well, you can try to use a PowerShell script, it's work in progress.

# User guide
Try one of these:

1. Open PowerShell ISE in administrator mode, paste the code, run the code.
2. Save the script code with .PS extension and run the script as PowerShell script with admin rights.

**PS: By default PowerShell execution policy is disabled**

Try to change it with: 

**`Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope LocalMachine`**

**`Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser`**

_It's advised to restrict the execution policy after finishing your job._
_For more info visit: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7.2_

## Getting the list of installed Windows Store packages

`Get-AppxPackage -AllUsers | Select Name`

**_Selects packages <by name> from locally <user account> installed packages_**

`Get-AppXProvisionedPackage -Online | Select DisplayName`

**_Selects packages <by name> from the new user packages._**

_Important: when creating new user profile Windows copies installed app packages into new user accounts. Remove the packages from the OS wide package list to dodge that behavior_

<the OS>

```mermaid
graph LR

a[Get-AppxPackage -AllUsers] --> b
b[Learn the list of installed bloatware packages] --> c
c[Add new package names to the script] --> d
d[Enjoy bloatware free experience]
```
