# Microsoft Defender Antivirus

**MAPS and features dependent on it disabled using this policy. It is quite invasive so I will only enable it for certain OUs.**

`Computer Configuration\Policies\Administrative Templates\Windows Components\Microsoft Defender Antivirus`

## MAPS

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MAPS`
- Join Microsoft MAPS -> Enabled -> Disabled

## Controlled Folder Access

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Controlled Folder Access`

- Configure Controlled folder access -> Enabled -> Block

## Attack Surface Reduction

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Attack surface reduction`

- Configure Attack Surface Reduction rules -> Add all rules from the [GUID Matrix](https://learn.microsoft.com/en-us/defender-endpoint/attack-surface-reduction-rules-reference?view=o365-worldwide#asr-rule-to-guid-matrix) except `01443614-cd74-433a-b99e-2ecdc07bfc25`. Set their value to 1.

Rationale: `01443614-cd74-433a-b99e-2ecdc07bfc25` depends on Microsoft Cloud Protection (MAPS). The only place where I use MAPS is my gaming machine, and it needs to be able to run not-so-reputable programs anyways.

**Warning:** NVIDIA Driver can fail installing because of `c0033c00-d16d-4114-a5a0-dc9b3a7d2ceb`, you can temporarily disable this ASR rule to update NVIDIA driver. The rule `56a863a9-875e-4185-98a7-b882c64b5ce5` is also worth keeping an eye on for NVIDIA drivers.

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
