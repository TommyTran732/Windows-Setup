# Registries

## Disable Co Installer

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Device Installer`

DisableCoInstallers -> REG_DWORD -> 1

https://www.bleepingcomputer.com/news/microsoft/how-to-block-windows-plug-and-play-auto-installing-insecure-apps/

## CVE-2023-24932

`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Secureboot`

AvailableUpdates -> REG_DWORD -> 30

https://support.microsoft.com/en-us/topic/kb5025885-how-to-manage-the-windows-boot-manager-revocations-for-secure-boot-changes-associated-with-cve-2023-24932-41a975df-beb2-40c1-99a3-b3ff139f832d