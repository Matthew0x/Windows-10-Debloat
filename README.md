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

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggTFJcblxuYVtHZXQtQXBweFBhY2thZ2UgLUFsbFVzZXJzXSAtLT4gYlxuYltMZWFybiB0aGUgbGlzdCBvZiBpbnN0YWxsZWQgYmxvYXR3YXJlIHBhY2thZ2VzXSAtLT4gY1xuY1tBZGQgbmV3IHBhY2thZ2UgbmFtZXMgdG8gdGhlIHNjcmlwdF0gLS0-IGRcbmRbRW5qb3kgYmxvYXR3YXJlIGZyZWUgZXhwZXJpZW5jZV0iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGFyayJ9LCJ1cGRhdGVFZGl0b3IiOnRydWUsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjp0cnVlfQ)](https://mermaid-js.github.io/mermaid-live-editor/edit/#eyJjb2RlIjoiZ3JhcGggTFJcblxuYVtHZXQtQXBweFBhY2thZ2UgLUFsbFVzZXJzXSAtLT4gYlxuYltMZWFybiB0aGUgbGlzdCBvZiBpbnN0YWxsZWQgYmxvYXR3YXJlIHBhY2thZ2VzXSAtLT4gY1xuY1tBZGQgbmV3IHBhY2thZ2UgbmFtZXMgdG8gdGhlIHNjcmlwdF0gLS0-IGRcbmRbRW5qb3kgYmxvYXR3YXJlIGZyZWUgZXhwZXJpZW5jZV0iLCJtZXJtYWlkIjoie1xuICBcInRoZW1lXCI6IFwiZGFya1wiXG59IiwidXBkYXRlRWRpdG9yIjp0cnVlLCJhdXRvU3luYyI6dHJ1ZSwidXBkYXRlRGlhZ3JhbSI6dHJ1ZX0)

```mermaid
graph LR

a[Get-AppxPackage -AllUsers] --> b
b[Learn the list of installed bloatware packages] --> c
c[Add new package names to the script] --> d
d[Enjoy bloatware free experience]
```
