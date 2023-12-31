# Device Guard

`Computer Configuration\Administrative Templates\System\Device Guard`

- Turn On Virtualization Based Security -> Enabled (**Only do this if you are running Windows on bare metal or with nested virtualization**)

1. Select Platform Security Level: Secure Boot and DMA Protection
2. Virtualization Based Protection of Code Integrity: Enabled with UEFI lock
3. Credential Guard Configuration: Enabled with UEFI lock
4. Secure Launch Configuration: Enabled
5. Kernel-mode Hardware-enforced Stack Protection: Enabled in enforcement mode