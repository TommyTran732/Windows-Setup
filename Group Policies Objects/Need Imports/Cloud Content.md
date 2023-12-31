# Cloud Content

I mostly disable all cloud content because they are way too annoying. There are also a few group policies relating to "personalization", so I am not entirely sure on the privacy implication of that either.

`Computer Configuration\Administrative Templates\Windows Components\Cloud Content`

- Turn off cloud optimized content -> Enabled
- Turn off cloud consumer account state content -> Enabled (**Does not show on Windows Server 2022 by default**)
- Do not show Windows tips -> Enabled
- Turn of Microsoft consumer experiences -> Enabled

`User Configuration\Administrative Templates\Windows Components\Cloud Content`

- Do not use diagnostic data for tailored experiences -> Enabled
- Turn off all Windows spotlight features -> Enabled
- Turn off the Windows Welcome Experience -> Enabled