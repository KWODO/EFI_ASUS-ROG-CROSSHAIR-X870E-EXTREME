Hackintosh EFI for ASUS ROG Crosshair X870E Extreme
----------------------------------------------------------------------------------------------------------------------

Link to the manufacturer's page: https://rog.asus.com/motherboards/rog-crosshair/rog-crosshair-x870e-extreme/

----------------------------------------------------------------------------------------------------------------------

This OpenCore-EFI works with macOS Ventura & macOS Sequoia
(not tested with macOS Sonoma).


----------------------------------------------------------------------------------------------------------------------
AUDIO:
----------------------------------------------------------------------------------------------------------------------
Realtek SupremeFX USB Audio (ALC4082) (VID_0B05&PID_1B7C)
X (OpenCore: AudioDxe.efi) (USB-Audio not supported)
√ (macOS Ventura/Sequoia: native) - rear: spdif-out, line-out, mic-in / front: line-out, mic-in


----------------------------------------------------------------------------------------------------------------------
ETHERNET:
----------------------------------------------------------------------------------------------------------------------
Realtek 5Gbit Network Adapter (RTL8126)
X (not supported in macOS) (Disabled in BIOS)

Aquantia/Marvell AQC113CS FastLinQ Edge 10Gbit Network Adapter (VEN_1D6A&DEV_04C0)
√ (macOS Ventura/Sequoia: native)


----------------------------------------------------------------------------------------------------------------------
WIFI:
----------------------------------------------------------------------------------------------------------------------
MediaTek Wi-Fi 7 BT5.3 (MT7927)
X (not supported in macOS) (removed from mainboard)


----------------------------------------------------------------------------------------------------------------------
USB-MAPPING:
----------------------------------------------------------------------------------------------------------------------
√ (macOS Ventura/Sequoia) (USBToolBox.kext + UTBMap_ROG-X870E-X.kext) or (USBMap_ROG-X870E-X.kext)

1x Front USB Type-C Port with switch (USB3.2) (U20G_C6 (1))
4x Front USB Type-A Ports (USB3.0) (U5G_E1234 (18))
2x Rear USB Type-C Port with switch (USB3.1) (U10G_C23/U10G_C22 (14))
8x Rear USB Type-A Ports (USB2.0) (U10G_3/U10G_4/U10G_18 (2) / U10G_19 (11) / U10G_20 (13) / U10G_9/U10G_8/U10G_21 (5))
1x Internal USB 2.0 Port for Bluetooth (WIFI-Module (15))
1x Internal USB 2.0 Port for USB Audio (6)(16)


----------------------------------------------------------------------------------------------------------------------
CPU:
----------------------------------------------------------------------------------------------------------------------
AMD Ryzen 9 7950X 4.5 GHz AM5*¹

iGPU AMD Radeon Graphics
X (disabled in BIOS)

*¹ CPU is set to ECO-Mode (maxed at 105W instead of 170W) (optional BIOS setting)


----------------------------------------------------------------------------------------------------------------------
RAM:
----------------------------------------------------------------------------------------------------------------------
Kingston FURY Beast DDR5-5200 MHz 288-Pin 128 GB Kit (4 x 32 GB)

KF552C40BBK-64 (2x)

(Default (JEDEC) configuration for 4 modules in dual channel running @ DDR5-3600 MHz)


----------------------------------------------------------------------------------------------------------------------
PCI EXPRESS CARDS:
----------------------------------------------------------------------------------------------------------------------
Sapphire TOXIC AMD Radeon RX 6950 XT Limited Edition 16 GB
√ (macOS Ventura/Sequoia) (whatevergreen.kext + Device Properties GPU-SPOOF)

PCIe-Slot1 (PCIEX16(G5)_1 (A))


----------------------------------------------------------------------------------------------------------------------
Broadcom BCM94360CD
√ (macOS Ventura: native)
√ (macOS Sequoia: OCLP)

M.2 NGFF Slot (WIFI-Module (15))

NGFF A+E Key to miniPCIe Adapter with 30cm FPC-Cable extension
miniPCIe WiFi 12+6Pin Adapter for Broadcom


----------------------------------------------------------------------------------------------------------------------
BOOTLOADER:
----------------------------------------------------------------------------------------------------------------------
OpenCore v1.0.5

----------------------------------------------------------------------------------------------------------------------




HINTS:
----------------------------------------------------------------------------------------------------------------------

-Generate your own "System Serial Number" and "System UUID" for this EFI-Files before using.
You can use OpenCoreConfigurator or similar.
It can be found in PlatformInfo/DataHub-Generic-PlatformNVRAM.

-If you want to use FileVault with OCLP-RootPatches (Fenvi T919),
enable "FileVault on Broken Seal"-Patch in Kernel/Patch.

-If you want to use supported RX 6000-Series GPU (without GPU-Spoof),
remove Device Properties for GPU.

----------------------------------------------------------------------------------------------------------------------

If anyone finds mistakes or has suggestions for improvement, please let me now, thank you :)
