# Group Policy Objects

- Make Central Store for policies: https://learn.microsoft.com/en-us/troubleshoot/windows-client/group-policy/create-and-manage-central-store
- Windows 23H2 template can be found here: https://www.microsoft.com/en-us/download/details.aspx?id=105667

The Default Domain Policy directory contains all of the policies I set domain wide. You can either apply them in the Default Domain Policy or break them up into multiple small ones. I split them into files in this repo so that it is easy to read.

Other directories contain the overrides I give to each Organizational Unit (OU). I do recommend breaking these down, as you might reuse the specific overrides across different OUs later on.