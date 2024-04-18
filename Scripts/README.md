# Scripts

- Put these in your NETLOGON directory
- In group policy objects, select the object you want to edit -> Computer Configuration -> Windows Setings -> Scripts -> Startup -> PowerShell Script, and add the scripts you want to use. Personally, I use all of these scripts in my Default Domain Policy object.

## Notes

- The DisableSMB1.ps1 script is not stricly necessary as SMB1 shouldn't be installed anyways. It's just there for extra assurances.