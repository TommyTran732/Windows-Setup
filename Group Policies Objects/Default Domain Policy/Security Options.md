# Security Options

Documentation: https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/settings-and-configuration?tabs=gpo

`Computer Configuration\Policies\Windows Settings\Security Settings\Local Policies\Security Options`

- User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode -> Prompt for credentials
- User Account Control: Only elevate executables that are signed and validated -> Enabled
- User Account Control: Switch to the secure desktop when prompting for elevation -> Enabled (Docs says it is enabled by default, but it is off on my Parallels VM somehow)
- Security setting -> Define -> Require signing (**Follow this guide to setup LDAPS if you do not have key server: https://www.dvolve.net/blog/2019/12/using-lets-encrypt-for-active-directory-domain-controller-certificates/**)