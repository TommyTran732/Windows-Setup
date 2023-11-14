# Windows Defender SmartScreen

`Computer Configuration\Administrative Templates\Windows Components\Windows Defender SmartScreen`

- Enhanced Phising Protection -> Service Enabled -> Disabled

**For a corporate scenario or when you cannot trust the user you are configuring it for and you choose to have SmartScreen enabled, do the followings:**,

- Explorer -> Configure Windows Defender SmartScreen -> Enabled -> Warn and prevent bypass
- Microsoft Edge -> Prevent bypassing Windws Defender SmartScreen prompts for sites -> Enabled

There is also Explorer -> Configure App Install Control that you might want to look into. Probably theatre though, it doesn't appear to block anything, or anything meaningful at least.