# MDM

`Computer Configuration\Administrative Templates\Windows Components\MDM`

Unless you run your own MDM system or something, this probably should not be on with a personal computer.

- Enable automatic MDM enrollment using default Azure AD credentials -> Disabled (Probably redundant because of the next policy, but it will also **unenroll** you from Azure AD)
- Disable MDM enrollment -> Enabled (This will not unenroll you though)