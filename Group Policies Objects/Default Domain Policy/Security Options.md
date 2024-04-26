# Security Options

Documentation: https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/settings-and-configuration?tabs=gpo

`Computer Configuration\Policies\Windows Settings\Security Settings\Local Policies\Security Options`

(**Follow this guide to setup LDAPS if you do not have key server: https://www.dvolve.net/blog/2019/12/using-lets-encrypt-for-active-directory-domain-controller-certificates/**)

- Accounts: Block Microsoft accounts -> Users can't add or log on with Microsoft accounts
- Accounts: Guest account status -> Disabled
- Devices: Prevent users from installing printer drivers -> Enabled
- Domain controller: LDAP server signing requirements: Require signing
- Domain controller: LDAP server channel binding token requirements: Always
- Domain member: Digitally encrypt or sign secure channel data (always) -> Enabled
- Domain member: Require strong (Windows 2000 or later) session key -> Enabled
- Microsoft network client: Digitally sign communications (always) -> Enabled
- Microsoft network server: Digitally sign communications (always) -> Enabled
- Network access: Allow anonymous SID/Name translation -> Disabled
- Network security: Do not store LAN Manager hash value on next password change -> Enabled
- Network security: Force logoff when logon hours expire -> Disabled
- Network security: LDAP client signing requirements: Require signing
- Network security: Restrict NTLM: Incoming NTLM traffic -> Deny all accounts
- Network security: Restrict NTLM: NTLM authentication in this domain -> Deny all
- Network security: Restrict NTLM: Outgoing NTLM traffic to remote servers -> Deny all
- Shutdown: Clear virtual memory pagefile -> Enabled
- User Account Control: Allow UIAccess applications to prompt for elevation without using the secure desktop -> Disabled
- User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode -> Prompt for credentials on the secure desktop
- User Account Control: Behavior of the elevation prompt for standard users -> Prompt for credentials on the secure desktop
- User Account Control: Only elevate executables that are signed and validated -> Enabled
- User Account Control: Only elevate UIAccess applications that are installed in secure locations -> Enabled
- User Account Control: Run all administrators in Admin Approval Mode
- User Account Control: Switch to the secure desktop when prompting for elevation -> Enabled
- User Account Control: Virtualize file and registry write failures to per-user locations -> Enabled