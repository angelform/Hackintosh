

# Hackintosh - macOS Big Sur 11.5 - Z370 + 8700 + RX 550

# Hardware

- CPU: Intel(R) CPU Core i7 8700
- Mainboard: Gigabyte Z370M-DS3H F14c
- RAM: hz (16GBx2@2666) 
- SSD:
    - Samsung SSD 850 EVO 500GB
    - Intel SSD 545s 400GB
- Wireless: Broadcom BCM943602CS  802.11ac + Bluetooth 4.1 (need to buy)
- VGA:
  - Intel HD Graphics 630 (Onboard)
  - MSI RX 550 2G GDDR5
- Monitors:
  - LG 27 inches 4K (3840x2160/60Hz)
- Power: Hipro 650w
- Mouse: Magic Trackpad 2
- Keyboard: Magic Keyboard

# Installation

This step extracts the Installer contents, then installs Clover bootloader to the USB stick.

  1. Insert the USB drive
  2. Open **/Applications/Utilities/Disk Utility**
  3. Highlight the USB drive in left column
  4. Click on the **Partition** tab
  5. Click **Current** and choose **1 Partition**
  6. Click **Options...**
  7. Choose **GUID Partition Table**
  8. Under **Name:** type **USB** (You can rename it later)
  9. Under **Format:** choose **Mac OS Extended (Journaled)**
  10. Click **Apply** then ***Partition***
  11. Open **/Applications/Utilities/Terminal**
  12. Type the following, enter password and hit enter. This command completely erases the USB, then creates native installer media from the Install macOS Application.

```sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/USB /Applications/Install\ macOS\ Big\ Sur.app --nointeraction```

  13. Copy **EFI** (USB) using the USB's EFI partition as the target volume.​

# BIOS
 BIOS version: [F14c] (https://www.gigabyte.ru/products/page/mb/z370m_ds3hrev_10#support-dl)

# What works
 - Intel HD Graphics 630 (Support Intel Quick Sync Video)
 - RX 550 AMD GPU
 - Ethernet (+ Wireless + Bluetooth)
 - USB 2.0/3.0 Ports
 - Sleep / Wake up
 - Sounds ?
 - Others (updating...)
# Benchmarks
## **Normal (4.7GHz)**

OS                    | CPU (Single-Core) | CPU (Multi-Cores) | OpenCL (KBL Graphics) | OpenCL (RX 580)
----------------------|:-----------------:|:-----------------:|:------------------:|:-------:
Big Sur (Geekbench 5) |throttling|throttling|[5409](1211633)|[44622](1211665)
Big Sur (Geekbench 4) |[6250](15630067)|[30135](15630067)|[24261](4863112)|[140718](4863107)
Catalina (Geekbench 5)|[1198](2932351)|[6233](2932351)|[5450](1211793)|[43108](1211263)
Catalina (Geekbench 4)|[6231](15629857)|[30069](15629857)|[24481](4863075)|[141787](4863077)

  \**Geekbench Browser* [here](https://browser.geekbench.com/v4/cpu/15630067)

# Credits
- Bootloaders + Kexts:
  - [OpenCore](https://github.com/acidanthera/OpenCorePkg)
  - [Acidanthera](https://github.com/acidanthera/OpenCorePkg)
- Forums
  - [dortania](https://dortania.github.io/OpenCore-Desktop-Guide)
  - [tonymacx86](https://www.tonymacx86.com)
  - [r/hackintosh](https://www.reddit.com/r/hackintosh)
