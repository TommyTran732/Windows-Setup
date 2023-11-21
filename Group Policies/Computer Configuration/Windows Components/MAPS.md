# MAPS

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus\MAPS`

Microsoft Defender Antivirus MAPS is an interesting case. You should configure it depending on your threat model, and treat it like SmartScreen. We will disable automatic sample submission regardless because that could be privacy invasive.

- Send file samples when further analysis is required -> Enabled -> Never send