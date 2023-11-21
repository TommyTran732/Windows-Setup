# Date & Time

Windows uses NTP for time synchronization, which is not secure due to the lack of encryption and authentication. If you are running bare metal, I recommend that you setup a VM to sync time using NTS, then use it as the NTP server for Windows. If you are running a VM (Parallels in my case), just disable network time synchronization and let the guest agent sync time from the host.