# Microsoft Defender Antivirus

**MAPS and features dependent on it disabled using this policy. It is quite invasive so I will only enable it for certain OUs.**

`Computer Configuration\Policies\Administrative Templates\Windows Components\Microsoft Defender Antivirus`

## MAPS

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MAPS`
- Join Microsoft MAPS -> Enabled -> Disabled

## Controlled Folder Access

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Controlled Folder Access`

- Configure Controlled folder access -> Enabled -> Block

## MpEngine

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MpEngine`

- Enable file hash computation feature -> Enabled

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