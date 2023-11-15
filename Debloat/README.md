# Debloating Windows

Windows mark a number of packages as "provisioned". Thus, they will persist in the system even when you right click and uninstall them or try to remove them through `winget`. Additionally, for apps installed from the Microsoft Store, they will continue existing in `C:\Program Files\WindowsApps` until it has been uninstalled by all users. `winget` also does not see packages installed by other users.

As such, if you want to make sure all of the annoying APPX/MSIX apps are gone, it is better to use `Get-AppxPackage`. The documentation is at https://learn.microsoft.com/en-us/powershell/module/appx/get-appxpackage?view=windowsserver2022-ps. `Get-AppxPackage` does not see Win32 packages, therefore you will still need to remove them using `winget` afterwards.

## Steps to debloat

- First, go to Settings -> Apps -> Optional features and remove unnecessary features. I personally remove everything here.

- Next, scroll to the bottom and click "More Windows Features". Turn Windows feautures on or off and remove Features that you don't need. On my Parallels VM, I removed everything except Microsoft Print to PDF. If you are running bare metal, you should keep HyperV, Microsoft Defender Application Guard, and Windows Sandbox on.

- Reboot the system

- Run the Windows Terminal as an Administrator

- To get a list of packages that can be removed, run `Get-AppxPackage -AllUsers | where {$_.NonRemovable -eq $false} | where {$_.isFramework -eq $false} | select Name,PackageFullName`.

- Run `Get-AppxPackage -AllUsers <PackageName> | Remove-AppxPackage -AllUsers` to remove the unwanted packages.

- "Uninstall" the remaining annoying apps from the Start Menu. They are not really apps on the system, they are just annoying shortcuts which will install the apps when you click on them. The list of packages I remove on my Parallels system is in the `Parallels.txt` file.

- Open the terminal and run `winget list` to see the remaining packages (note that this will not exclude Framework packages). Remove the remaining undesirable apps with `winget remove <PackageName>`. In most cases, this will just be OneDrive.