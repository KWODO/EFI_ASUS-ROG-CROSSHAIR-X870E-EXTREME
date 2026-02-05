# Hackintosh EFI for<br/>ASUS ROG CROSSHAIR X870E EXTREME
Link to the manufacturer's page [here](https://rog.asus.com/motherboards/rog-crosshair/rog-crosshair-x870e-extreme/)

![https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/main/UTBUSBMap_ROG-X870E-X.png](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ASUS-ROG-CH-X870E-X_MAINBOARD.png)

----------------------------------------------------------------------------------------------------------------------
## <ins>BIOS:</ins>
### Version 1605 (2025/07/22)<br/>
### Version 1715 (2025/09/25)<br/>
Link to the manufacturer's BIOS & Firmware page [here](https://rog.asus.com/motherboards/rog-crosshair/rog-crosshair-x870e-extreme/helpdesk_bios/)

:white_check_mark: (macOS Ventura/Sequoia) *(OpenCore AMD-Patches + ACPI-Patches by CorpGhost)*

### BIOS MOD<br/>
- Removed the ASUS ROG Boot Splash Screen / replaced with a plain/black one<br/>

Guide:<br/>
1.) Download UEFITool_0.28.0 WIN/MAC, run UEFITool.exe/UEFITool.app<br/>
2.) Open Image File (Ctrl+O/⌘+O), select BIOS file<br/>
3.) Search (Ctrl+F/⌘+F), select tab labeled "GUID", input 7BB28B99-61BB-11D5-9A5D-0090273FC14D<br/>
4.) Double-click on the line of GUID pattern in Messages "7BB28B99-61BB-11D5-9A5D-0090273FC14D"<br/>
5.) Press on expand > "7BB28B99-61BB-11D5-9A5D-0090273FC14D" (File/Freeform/Logo.bmp)<br/>
6.) Press on expand > "EE4E5898-3914-4259-9D6E-DC7BD79403CF" (Section/GUID defined)<br/>
7.) Right click on "Raw section" line (Section/Raw), "Extract body..." and save it as Logo.raw<br/>
8.) Rename the Logo.raw file to Logo.bmp<br/>
9.) Edit the image and save it<br/>
10.) Rename the image extension to .raw<br/>
11.) Right click on "Raw section" line, "Replace body..." and select the new Logo.raw file<br/>
12.) Ctrl+S to save the BIOS<br/>
13.) Done! Flash your new modiefied BIOS.<br/>

----------------------------------------------------------------------------------------------------------------------
## <ins>AUDIO:</ins>
### Realtek SupremeFX OnBoard USB Audio (ALC4082)<br/>
`VID_0B05&PID_1B7C`<br />

:x: (OpenCore: AudioDxe.efi) *(USB-Audio not supported)*<br />
:white_check_mark: (macOS Ventura/Sequoia: native) `rear: spdif-out, line-out, mic-in` `front: line-out, mic-in`

----------------------------------------------------------------------------------------------------------------------
## <ins>ETHERNET:</ins>
### Realtek 5Gbit Network Adapter (RTL8126)<br />
`VEN_10EC&DEV_8126`<br />

:white_check_mark: (macOS Ventura/Sequoia) *(SimpleRTK5.kext)
https://github.com/laobamac/SimpleRTK5

### Aquantia/Marvell FastLinQ Edge 10Gbit Network Adapter (AQC113CS)<br/>
`VEN_1D6A&DEV_04C0`<br />

:white_check_mark: (macOS Ventura/Sequoia) *(OpenCore Kernel-Quirk + Kernel-Patches "Set 1")*

----------------------------------------------------------------------------------------------------------------------
## <ins>WIFI:</ins>
### MediaTek Wi-Fi 7 BT5.3 (MT7927)<br/>
:x: (not supported in macOS) **(removed from mainboard)**

----------------------------------------------------------------------------------------------------------------------
## <ins>USB-MAPPING:</ins>

:white_check_mark: (macOS Ventura/Sequoia)<br/>
(USBToolBox.kext + UTBMap_ASUS-ROG-CH-X870E-X.kext) or (USBMap_ASUS-ROG-CH-X870E-X.kext)<br/>

1x Front USB Type-C Port with switch (USB3.2)<br/>
`U20G_C6 (1)`<br/>

4x Front USB Type-A Ports (USB3.0)<br/>
`U5G_E1234 (18)`<br/>

2x Rear USB Type-C Port with switch (USB3.1)<br/>
`U10G_C23/U10G_C22 (14)`<br/>

8x Rear USB Type-A Ports (USB2.0)<br/>
`U10G_3/U10G_4/U10G_18 (2)` `U10G_19 (11)` `U10G_20 (13)` `U10G_9/U10G_8/U10G_21 (5)`<br/>

1x Internal USB 2.0 Port for Bluetooth<br/>
`M.2(WIFI) (15)`<br/>

1x Internal USB 2.0 Port for USB Audio<br/>
`Audio (6)(16)`<br/>

![https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/main/UTBUSBMap_ROG-X870E-X.png](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/UTBUSBMap_ASUS-ROG-CH-X870E-X.png)

![[https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/main/UTBUSBMap_ROG-X870E-X.png](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/Hackintool-USB.png)](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/Hackintool-USB.png)

### ASMedia USB4 Host Controller (ASM4242)<br/>
`VEN_1B21&DEV_2425`<br/>

:x: (not supported in macOS)

----------------------------------------------------------------------------------------------------------------------
## <ins>CPU:</ins>
### AMD Ryzen 9 7950X 4.5 GHz AM5*¹

iGPU AMD Radeon Graphics<br/>
:x: (not supported in macOS) **(disabled in BIOS)**

*¹ CPU is set to PBO-Enhanced (Level 2 80°C 170W) (optional BIOS setting)

----------------------------------------------------------------------------------------------------------------------
## <ins>RAM:</ins>
### Kingston FURY Beast DDR5-5200 MHz 288-Pin 128 GB Kit (4 x 32 GB)

KF552C40BBK4-128

(Default (JEDEC) configuration for 4 modules in dual channel running @ 3600 MHz / CL 30-29-29-58 / 1.10v)

----------------------------------------------------------------------------------------------------------------------

## <ins>PCI EXPRESS CARDS:</ins>
### Sapphire TOXIC AMD Radeon RX 6950 XT Limited Edition 16 GB<br/>
`VEN_1002&DEV_73A5`<br/>

:white_check_mark: (macOS Ventura/Sequoia) *(whatevergreen.kext + Device Properties GPU-SPOOF)*

PCIe-Slot1 `PCIEX16(G5)_1 (A)`

### Broadcom BCM94360CD 802.11ac Wireless Network Adapter with Bluetooth 4.0<br/>
`VEN_14E4&DEV_43A0`<br/>

:white_check_mark: (macOS Ventura: native)<br/>
:white_check_mark: (macOS Sequoia: OCLP)

M.2 NGFF Slot `M.2(WIFI) (15)`<br/>

NGFF A+E Key to miniPCIe Adapter with 30cm FPC-Cable extension<br/>
![https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/M2-NGFF_miniPCIe_AdapterCard-Extension.png](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/M2-NGFF_miniPCIe_AdapterCard-Extension.png)

miniPCIe WiFi 12+6Pin Adapter for Broadcom<br/>
![https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/miniPCIe_BCM94630_AdapterCard.png](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/miniPCIe_BCM94630_AdapterCard.png)

----------------------------------------------------------------------------------------------------------------------
## <ins>BOOTLOADER:</ins>
### OpenCore v1.0.5<br />

OpenCore-Debug EFI for ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605/1715 _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/OC105-DEBUG_ASUS-ROG-CH-X870E-X_BIOS-1605-1715_V1.0_NoSN.zip)<br />

----------------------------------------------------------------------------------------------------------------------
## <ins>Kernel Extensions:</ins>

Lilu _by acidanthera_ [here](https://github.com/acidanthera/Lilu)<br />
WhateverGreen _by acidanthera_ [here](https://github.com/acidanthera/WhateverGreen)<br />
VirtualSMC _acidanthera_ [here](https://github.com/acidanthera/VirtualSMC)<br />
FeatureUnlock _acidanthera_ [here](https://github.com/acidanthera/FeatureUnlock)<br />
RestrictEvents _by acidanthera_ [here](https://github.com/acidanthera/RestrictEvents)<br />
NVMeFix _by acidanthera_ [here](https://github.com/acidanthera/NVMeFix)<br />
USBToolBox _by Dhinak G_ [here](https://github.com/USBToolBox/kext)<br />
AppleMCEReporterDisabler _by XLNCs_ [here](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip)<br />
AMFIPass _by Dhinak G_ [here](https://github.com/kaoskinkae/AMFIPass)<br />
IOSkywalkFamily (from macOS Sonoma 14.4<br />
IO80211FamilyLegacy (from macOS Sonoma 14.4<br />
SMCProcessorAMD _by macos86_ [here](https://github.com/macos86/SMCProcessorAMD) (only up to macOS Sonoma 14.x)<br />

----------------------------------------------------------------------------------------------------------------------
### <ins>HINTS:</ins>

- Generate your own "System Serial Number" and "System UUID" for this EFI-Files before using.<br/>
You can use OpenCoreConfigurator or similar.<br/>
It can be found in PlatformInfo/DataHub-Generic-PlatformNVRAM.<br/>

- Create your own "MmioWhitelist" using OpenCore-Debug + MmioDevirt _by CorpNewt_ [here](https://github.com/corpnewt/MmioDevirt)<br />
Link to Dortania Guide page [here](https://dortania.github.io/OpenCore-Install-Guide/extras/kaslr-fix.html#so-what-is-kaslr)<br />
Link to EliteMacx86 Guide page [here](https://elitemacx86.com/threads/how-to-fix-kaslr-slide-values.2037/)<br />

- If you want to use supported RX 6000-Series GPU,<br/>
remove Device Properties for GPU-Spoofing.

- (OPTIONAL) If you want to use FileVault with OCLP-RootPatches (WIFI),<br/>
enable "FileVault on Broken Seal"-Patch in Kernel/Patch.

----------------------------------------------------------------------------------------------------------------------
### <ins>TOOLS I USED TO CREATE:</ins>

OpenCore Bootloader _by Acidanthera_ [here](https://github.com/acidanthera/OpenCorePkg)<br />

AMD-Vanilla-Patches _by CorpNewt_ [here](https://github.com/corpnewt/AMDVanillaPatches)<br />

SSDTTime _by CorpNewt_ [here](https://github.com/corpnewt/SSDTTime)<br />
<sup>SSDTTime Results for ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605 _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/SSDTTime_Results_ASUS-ROG-CH-X870E-X_BIOS-1605.zip)</sup><br />

ACPI-Patches for ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605/1715 _by CorpGhost_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ACPI-Patches_ASUS-ROG-CH-X870E-X_BIOS-1605-1715_by-CorpGhost.zip)<br />

MmioDevirt _by CorpNewt_ [here](https://github.com/corpnewt/MmioDevirt)<br />

USBToolBox _by Dhinak G_ [here](https://github.com/USBToolBox/tool)<br />
<sup>USBToolBox Settings+Mapping for ASUS ROG CROSSHAIR X870E EXTREME _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/USBToolBox-Settings-Mapping_ASUS-ROG-CH-X870E-X.zip)</sup><br />

Aquantia-macOS-Patches _by CaseySJ_ [here](https://github.com/CaseySJ/Aquantia-macOS-Patches)<br />

UEFITool v0.28.0 WIN/MAC _by LongSoft_ [here](https://github.com/LongSoft/UEFITool/releases/tag/0.28.0)<br />

ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605 MOD (CAP-File) _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ASUS-ROG-CH-X870E-X-BIOS-1605-MOD.CAP.zip)<br />
ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1715 MOD (CAP-File) _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ASUS-ROG-CH-X870E-X-BIOS-1715-MOD.CAP.zip)<br />
<sup>My BIOS-Settings (TXT + CMO-File) for BIOS 1605/1715 _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/BIOS-1605-1715_Settings_KWODO_ASUS-ROG-CH-X870E-X.zip)</sup><br />

----------------------------------------------------------------------------------------------------------------------
### <ins>USEFUL UTILITIES:</ins>

gibMacOS _by CorpNewt_ [here](https://github.com/corpnewt/gibMacOS)<br />
gibMacRecovery _by CorpNewt_ [here](https://github.com/corpnewt/gibMacRecovery)<br />
USB-Installer-Creator _by CorpNewt_ [here](https://github.com/corpnewt/USB-Installer-Creator)<br />
GenSMBIOS _by CorpNewt_ [here](https://github.com/corpnewt/GenSMBIOS)<br />
CheckPCI _by CorpNewt_ [here](https://github.com/corpnewt/CheckPCI)<br />
CheckGPU _by CorpNewt_ [here](https://github.com/corpnewt/CheckGPU)<br />
CheckAudio _by CorpNewt_ [here](https://github.com/corpnewt/CheckAudio)<br />
LogCheck _by CorpNewt_ [here](https://github.com/corpnewt/LogCheck)<br />
DevicePath _by CorpNewt_ [here](https://github.com/corpnewt/DevicePath)<br />
GetUUID _by CorpNewt_ [here](https://github.com/corpnewt/GetUUID)<br />
OCConfigCompare _by CorpNewt_ [here](https://github.com/corpnewt/OCConfigCompare)<br />
ProperTree _by CorpNewt_ [here](https://github.com/corpnewt/ProperTree)<br />
IORegistryExplorer _by vulgo_ [here](https://github.com/vulgo/IORegistryExplorer)<br />
Hackintool _by benbaker76_ [here](https://github.com/benbaker76/Hackintool)<br />
Hackintool Updated PCI-IDs for ASUS ROG CROSSHAIR X870E EXTREME _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/Hackintool_PCI-IDS-Update_ASUS-ROG-CH-X870E-X.zip)<br />
OCAuxiliaryTools OCAT _by ic005k_ [here](https://github.com/ic005k/OCAuxiliaryTools)<br />
OpenCore Configurator _by mackie1000projects_ [here](https://mackie100projects.altervista.org/)<br />
About-This-Hack _by 0xCUB3_ [here](https://github.com/2009-Nissan-Cube/About-This-Hack)<br />

----------------------------------------------------------------------------------------------------------------------
If anyone finds mistakes or has suggestions for improvement,<br/>
please let me now, thank you :)
[AMD-OSX Forum](https://forum.amd-osx.com/threads/success-asus-rog-crosshair-x870e-extreme-ryzen-9-7950x-rx-6950xt-dual-boot-macos-ventura-windows-11.6048/#post-42959)<br />
----------------------------------------------------------------------------------------------------------------------
