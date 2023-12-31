# Bitlocker Drive Encryption

`Computer Configuration\Administrative Templates\Windows Components\Bitlocker Drive Encryption`

Choose drive encryption method and cipher strength-> Enable -> XTS-AES 256-bit for operating system, fixed data, and removable drives. For Windows Vista, Windows Server 2008, etc... use AES 256-bit.

**The disable new DMA devices when computer is locked should only be enabled if the specific computer does not support kernel DMA protection. Do not set this at the domain level.**

## Operating System Drives

- Disallow standard users from changing the PIN or password -> Enabled
- Require additional authentication at startup -> Enabled -> Do not allow TPM, Allow startup PIN with TPM, Do not allow startup key with TPM, Allow startup key and PIN with TPM. (**This is especially important as we do not want the TPM to automatically release the encryption key at boot.**)
- Allow enhanced PINs for startup -> Enabled.
- Configure TPM platform validation profile for native UEFI firmware configurations -> Enabled -> PCR 0,1,2,3,3,4,5,6,7,11