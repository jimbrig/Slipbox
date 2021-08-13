---
Creation Date: 2021-08-13 03:40
Last Modified Date: Friday 13th August 2021 03:40:35
Author: Jimmy Briggs <jimbrig1993@outlook.com>
Alias: How to Resolve PIN Issues in Windows
Tags: ["#Topic/Development/PowerShell", "#Topic/Computer/Windows"]
---

# How to Resolve PIN Issues in Windows

`icacls C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc /T /Q /C /RESET`

```powershell
runas /profile /user:JIMMYSMSI\jimbr 'pwsh.exe'

# in new terminal running as jimbr:
Take-Ownership C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc

icacls C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc /T /Q /C /RESET
```


alternatively, from the [[Windows Recovery Environment (winRE)]] pre-boot screen select Troubleshoot > Command Prompt and run `icacls C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc /T /Q /C /RESET`.


***

Links: [[Run Commands as Another User Account - RUNAS]]

Sources:
- [How to Fix Windows 10 Pin Issues when Logging In - Appuals.com](https://appuals.com/how-to-fix-windows-10-pin-issues-when-logging-in/#:~:text=How%20to%20Fix%20Windows%2010%20Pin%20Issues%20when,4%20Method%204%3A%20Use%20a%20Local%20Account.%20)

