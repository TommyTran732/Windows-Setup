# LDAPS

**Only relevant if you are using Active Directory.**

Active Directory by default only uses LDAP, which is unencrypted and unverified. You should set up LDAPS. Traditionally, you have to setup a server for key management. However, if you only have Domain Controllers, you may be able to get away with this guide: https://www.dvolve.net/blog/2019/12/using-lets-encrypt-for-active-directory-domain-controller-certificates/