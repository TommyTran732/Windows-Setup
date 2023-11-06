# Microsoft Edge Group Policy

`Computer Configuration\Administrative Templates\Windows Components\Microsoft Edge`

**For some reason this does not seem to take effect - needs checking**

Configure Autofill -> Disable (Password Manager is off so no reason for autofill to be on)
Configure Do Not Track -> Enable
Allow Extensions -> Disable (I do not use extensions, and they reduce security in a lot of cases. Don't disable this if you need extensions, of course.)
Allow Adobe Flash -> Disable (Dead technology, dangerous)
Configure Password Manager -> Disable (**The password manager does NOT have E2EE**)
Prevent using Localhost IP address for WebRTC -> Enable