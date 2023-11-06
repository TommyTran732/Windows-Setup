# Bitlocker Drive Encryption

`Computer Configuration\Administrative Templates\Windows Component\Bitlocker Drive Encryption`

Choose drive encryption method and cipher strength (Windows 10 [Version 1511] and later) -> Enable -> XTS-AES 256-bit for operating system, fixed data, and removable drives.

## Operating System Drives

Require additional authentication at startup -> Enabled -> Do not allow TPM, Allow startup PIN with TPM, Do not allow startup key with TPM, Allow startup key and PIN with TPM. (**This is especially important as we do not want the TPM to automatically release the encryption key at boot.**)
Allow enhanced PINs for startup -> Enabled.
