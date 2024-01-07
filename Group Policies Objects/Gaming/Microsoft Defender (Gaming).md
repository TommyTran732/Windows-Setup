# Microsoft Edge

`Computer Configuration\Policies\Administrative Templates\Microsoft Edge`

- SmartScreen settings -> Configure Microsoft Defender SmartScreen -> Enabled
- SmartScreen settings -> Configure Microsoft SmartScreen to block potentially unwanted apps -> Enabled
- TyposuqattingChecker settings -> Configure Edge TyposquattingChecker -> Enabled


# Microsoft Defender Antivirus

## MAPS

`Computer Configuration\Policies\Administrative Templates\Windows Components\Microsoft Defender Antivirus`
- Join Microsoft MAPS -> Enabled -> Advanced Membership
- Configure the 'Block at First Sight' feature -> Enabled
- Send file samples when further analysis is required -> Enabled -> Always Prompt (Send safe sample works better with 'Block at First Sight, but I really, really do not trust Microsoft on this one)

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

- Configure extended cloud check -> Specify the extended cloud check time in seconds -> 50
- Select cloud protection level -> Zero tolerance blocking level


# Windows Defender SmartScreen

`Computer Configuration\Policies\Administrative Templates\Windows Components\Windows Defender SmartScreen`

- Explorer -> Configure Windows Defender SmartScreen -> Enabled -> Warn
- Microsoft Edge -> Configure Windows Defender SmartScreen -> Enabled
