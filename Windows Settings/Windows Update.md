# Windows Update

Make sure the followings are selected:

- Uncheck update as soon as possible (this is essentially the same as auto update with gradual release - we will configure the group pol to be auto update without gradual release)
- Advanced option -> Receive updates for other Microsoft products
- Notify when restart is required to finish updating
- Install optional updates

# Microsoft Store Shenanigans

- If you are using Parallels, make sure to install Parallels Tools to enable the Microsoft Store.
- Go to the Microsoft Store and update all apps. Apps are outdated almost by guarantee. If winget is acting finicky, this might just be because it is not updated.

Think about whether you want to login with a Microsoft Account with or not. If you do not login, app installs are tied to your hardware ID. If you do, then they will be tied to your Microsoft Account.
