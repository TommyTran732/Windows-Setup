# Getting an ISO

If you want to get an x64/x86 enterprise ISO, follow https://www.thewindowsclub.com/download-windows-10-enterprise-iso-with-media-creation-tool

Essentially, the command to use with the Windows Media creation tool is `/Eula Accept Retail /MediaArch x64 /MediaLangCode en-US /MediaEdition Enterprise`.

Microsoft does not distribute Windows ARM ISOs as far as I know. The basic procedure is to download some ESD files from Microsoft, then convert it into an ISO.

If you use Parallels, just let it create a Windows VM automatically. It will make an Windows ARM Home/Pro ISO in your Downloads Folder, and you can use that for a manual installation later.

Another easy option is to use CrystalFetch on macOS to build the ISOs.