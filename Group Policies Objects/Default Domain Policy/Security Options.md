# Security Options

Documentation: https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/settings-and-configuration?tabs=gpo

`Computer Configuration\Policies\Windows Settings\Security Settings\Local Policies\Security Options`

- Domain controller: LDAP server signing requirements: Require signing (**Follow this guide to setup LDAPS if you do not have key server: https://www.dvolve.net/blog/2019/12/using-lets-encrypt-for-active-directory-domain-controller-certificates/**)
- Domain controller: LDAP server channel binding token requirements: Always
- Microsoft network client: Digitally sign communications: Always
- Network security: LDAP client signing requirements: Require signing
- Shutdown: Clear virtual memory pagefile -> Enabled
- User Account Control: Allow UIAccess applications to prompt for elevation without using the secure desktop -> Disabled
- User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode -> Prompt for credentials on the secure desktop
- User Account Control: Behavior of the elevation prompt for standard users -> Prompt for credentials on the secure desktop
- User Account Control: Only elevate executables that are signed and validated -> Enabled
- User Account Control: Only elevate UIAccess applications that are installed in secure locations -> Enabled
- User Account Control: Run all administrators in Admin Approval Mode
- User Account Control: Switch to the secure desktop when prompting for elevation -> Enabled
- User Account Control: Virtualize file and registry write failures to per-user locations -> Enabled