#### Installieren
* `& <path_to_exe>`

#### Deinstallieren
* `$MyApp = Get-WmiObject -Class Win32_Product | Where-Object{$_.Name -eq "Application Name"}`-> `$MyApp.Uninstall()`
#### Commands
Str + R -> Suchen