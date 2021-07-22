# AMD Hackintosh OpenCore configuration
This repository acts as a storage for my OpenCore configuration for macOS 11.x Big Sur running on the Asus Crosshair VIII Hero (WiFi) X570 motherboard with an AMD Ryzen 5900x and Radeon 6800.

DO NOT attemt to use this EFI if you do not know what you're doing. I believe this configuration should work with any Asus X570 motherboards with a big navi GPU. But I take no responsibility for any damage that may be caused if you do not audit this configuration before using it.
## Platform Info (SMBios) - Required
The `config.plist` file requires information about your mac hardware. You will need to add information before attempting to use this opencore EFI. This plist is configured as a `MacPro7,1`.

In order to generate serial information, use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate valid serial numbers and populate them in the `config.plist` file.

## BIOS Configuration
- Start by resetting bios to just -> Load Optimised Defaults
- Ai Tweaker -> D.O.C.P.
- Advanced -> APM Configuration -> Power On By PCIe -> Enabled
- Advanced -> PCI Subsystem Settings -> Above 4G Decoding -> Enabled
- Advanced -> PCI Subsystem Settings -> Re-Size BAR Support -> Disabled
- Advanced -> USB Configuration -> Legacy USB Support -> Auto or Disabled
- Boot -> Boot Configuration -> Fast boot -> Disabled
- Boot -> CSM -> Launch CSM -> Disabled
- Boot -> Secure boot -> OS Type -> Windows UEFI mode
- Boot -> Secure boot -> Key Management -> Clear Secure Boot Keys
