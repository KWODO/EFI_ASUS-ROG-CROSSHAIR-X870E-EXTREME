# Hackintosh EFI for<br/>ASUS ROG CROSSHAIR X870E EXTREME
Link to the manufacturer's page [here](https://rog.asus.com/motherboards/rog-crosshair/rog-crosshair-x870e-extreme/)

----------------------------------------------------------------------------------------------------------------------
## <ins>BIOS:</ins>
### Version 1605 (2025/07/22)<br/>
Link to the manufacturer's BIOS & Firmware page [here](https://rog.asus.com/motherboards/rog-crosshair/rog-crosshair-x870e-extreme/helpdesk_bios/)

:white_check_mark: (macOS Ventura/Sequoia) *(OpenCore AMD-Patches + ACPI-Patches by CorpGhost)*

### Version 1605 MOD (2025/07/22)<br/>
- Removed the ASUS ROG Boot Splash Screen / replaced with a plain/black one<br/>

Link to Reddit Guide page [here](https://www.reddit.com/r/pcmasterrace/comments/nl5ood/guide_how_to_set_a_custom_boot_logo_on_a_modern/)

:white_check_mark: (macOS Ventura/Sequoia) *(OpenCore AMD-Patches + ACPI-Patches by CorpGhost)*

----------------------------------------------------------------------------------------------------------------------
## <ins>AUDIO:</ins>
### Realtek SupremeFX OnBoard USB Audio (ALC4082)<br/>
`VID_0B05&PID_1B7C`<br />

:x: (OpenCore: AudioDxe.efi) *(USB-Audio not supported)*<br />
:white_check_mark: (macOS Ventura/Sequoia: native) `rear: spdif-out, line-out, mic-in` `front: line-out, mic-in`

----------------------------------------------------------------------------------------------------------------------
## <ins>ETHERNET:</ins>
### Realtek 5Gbit Network Adapter (RTL8126)<br />
:x: (not supported in macOS) **(Disabled in BIOS)**

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

*¹ CPU is set to ECO-Mode (maxed at 105W instead of 170W) (optional BIOS setting)

----------------------------------------------------------------------------------------------------------------------
## <ins>RAM:</ins>
### Kingston FURY Beast DDR5-5200 MHz 288-Pin 128 GB Kit (4 x 32 GB)

KF552C40BBK-64 (2x)

(Default (JEDEC) configuration for 4 modules in dual channel running @ DDR5-3600 MHz)

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

OpenCore-Debug EFI for ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605 _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/OC105-DEBUG_ASUS-ROG-CH-X870E-X_BIOS-1605_V1.0_NoSN.zip)<br />

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

ACPI-Patches for ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605 _by CorpGhost_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ACPI-Patches_ASUS-ROG-CH-X870E-X_BIOS-1605_by-CorpGhost.zip)<br />

MmioDevirt _by CorpNewt_ [here](https://github.com/corpnewt/MmioDevirt)<br />

USBToolBox _by Dhinak G_ [here](https://github.com/USBToolBox/tool)<br />
<sup>USBToolBox Settings+Mapping for ASUS ROG CROSSHAIR X870E EXTREME _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/USBToolBox-Settings-Mapping_ASUS-ROG-CH-X870E-X.zip)</sup><br />

Aquantia-macOS-Patches _by CaseySJ_ [here](https://github.com/CaseySJ/Aquantia-macOS-Patches)<br />

UEFITool v0.28.0 _by LongSoft_ [here](https://github.com/LongSoft/UEFITool)<br />
ASUS ROG CROSSHAIR X870E EXTREME - BIOS 1605 MOD (CAP-File) _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/ASUS-ROG-CH-X870E-X-BIOS-1605-MOD.CAP.zip)<br />
My BIOS-Settings (TXT + CMO-File) for BIOS 1605 _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/BIOS-1605_Settings_KWODO_ASUS-ROG-CH-X870E-X.zip)<br />

----------------------------------------------------------------------------------------------------------------------
### <ins>USEFUL UTILITIES:</ins>

CheckPCI _by CorpNewt_ [here](https://github.com/corpnewt/CheckPCI)<br />
CheckGPU _by CorpNewt_ [here](https://github.com/corpnewt/CheckGPU)<br />
CheckAudio _by CorpNewt_ [here](https://github.com/corpnewt/CheckAudio)<br />
LogCheck _by CorpNewt_ [here](https://github.com/corpnewt/LogCheck)<br />
DevicePath _by CorpNewt_ [here](https://github.com/corpnewt/DevicePath)<br />
GetUUID _by CorpNewt_ [here](https://github.com/corpnewt/GetUUID)<br />
OCConfigCompare _by CorpNewt_ [here](https://github.com/corpnewt/OCConfigCompare)<br />
ProperTree _by CorpNewt_ [here](https://github.com/corpnewt/ProperTree)<br />
Hackintool _by benbaker76_ [here](https://github.com/benbaker76/Hackintool)<br />
Hackintool Updated PCI-IDs for ASUS ROG CROSSHAIR X870E EXTREME _by KWODO_ [here](https://github.com/KWODO/EFI_ASUS-ROG-CROSSHAIR-X870E-EXTREME/blob/main/Hackintool_PCI-IDS-Update_ASUS-ROG-CH-X870E-X.zip)<br />

----------------------------------------------------------------------------------------------------------------------
If anyone finds mistakes or has suggestions for improvement,<br/>
please let me now, thank you :)
----------------------------------------------------------------------------------------------------------------------
