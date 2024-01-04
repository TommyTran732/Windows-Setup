# Microsoft Defender Antivirus

**MAPS and features dependent on it are not enabled using this policy. It just configures how aggressive MAPS should be. This is quite invasive so I will only enable it for certain OUs.**

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus`

## MAPS

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MAPS`

- Configure the 'Block at First Sight' feature -> Enabled
- Send file samples when further analysis is required -> Enabled -> Always Prompt (Send safe sample works better with 'Block at First Sight, but I really, really do not trust Microsoft on this one)

## Controlled Folder Access

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Controlled Folder Access`

- Configure Controlled folder access -> Enabled -> Block

## Network Protection

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Network Protection`

Only relevant if SmartScreen is used.

Documentation:
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/network-protection?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/enable-network-protection?view=o365-worldwide

This settings controls whether Network protection is allowed to be configured into block or audit mode on Windows -> Enabled (Only relevant if running Windows Server)
Prevent users and apps from accessing dangerous websites -> Enabled -> Block

## MpEngine

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MpEngine`

Only relevant if MAPS is used

- Enable file hash computation feature -> Enabled
- Configure extended cloud check -> Specify the extended cloud check time in seconds -> 50
- Select cloud protection level -> Zero tolerance blocking level

## Quarantine

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Quarantine`

- Configure local settings override for the removal of items from Quarantine folder -> Enabled
- Configure removal of items from Quarantine folder -> 1 day

## Scan

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Scan`

- Scan for the latest virus and spyware security intelligence before running a scheduled scan -> Enabled
- Turn on catch-up quick scan -> Enabled

## Security Intelligence Updates

- Check for the latest virus and spyware security intelligence on startup -> Enabled