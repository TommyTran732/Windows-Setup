# Microsoft Edge

`Computer Configuration\Policies\Administrative Templates\Microsoft Edge`

You will need to download the Edge policies from https://www.microsoft.com/en-us/edge/business/download?form=MA13FJ and install it.

For the actual policies to set, you can follow my repo at https://github.com/TommyTran732/Microsoft-Edge-Policies at set the equivalent group policies of what is being set there. I will try to document them below, but it is quite a lot.

SmartScreen and Typosquatting as recommeded settings doesn't seem to apply consistently, therefore I force them to be disabled in my Domain Default Policy.

- Cast -> Enabled Google Cast -> Disabled (EnableMediaRouter": false)
- Content Settings -> Block cookies on specific sites -> ntp.msn.com ("CookiesBlockedForUrls": [ "ntp.msn.com" ])
- Content Settings -> Default geolocation setting -> Enabled -> Don't allow any site to track users' physical location ("DefaultGeolocationSetting": 2)
- Content Settings -> Control use of insecure content Exceptions -> Enabled -> Do not allow any sites to load mixed content ( "DefaultInsecureContentSetting": 2)
- Content Settings -> Configure cookies -> Enabled -> Keep cookies for the duration of the session, except ones listed in "SaveCookiesOnExit" (DefaultCookiesSetting": 4)
- Content Settings -> Default setting for third-party storage partitioning -> Let third-party storage partitioning to be enabled. ("DefaultThirdPartyStoragePartitioningSetting": 1)
- Content Settings -> Control the use of File System API for reading -> Don't allow any site to request and read access to files and directories via the File System API ("DefaultFileSystemReadGuardSetting": 2)
- Content Settings -> Control the use of File System API for writing -> Don't allow any site to request and write access to files and directories via the File System API ("DefaultFileSystemWriteGuardSetting": 2)
- Content Settings -> Control use of the Web Bluetooth API -> Don't allow any site to request access to Bluetooth devices via the Web Bluetooth API ("DefaultWebBluetoothGuardSetting": 2)
- Content Settings -> Allow notifications to set Microsoft Edge as default PDF reader -> Disabled ("ShowPDFDefaultRecommendationsEnabled": false)