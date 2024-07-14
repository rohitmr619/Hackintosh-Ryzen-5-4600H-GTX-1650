# Hackintosh Ryzen 5 4600H-GTX 1650

## Overview

This repository provides EFI configurations and instructions to install macOS on the Lenovo IdeaPad Gaming 3 using OpenCore bootloader. The configuration has disabled the Nvidia GTX 1650 GPU due to incompatibility with macOS. Below is a summary of the hardware support status:

| Component         | Status                  |
|-------------------|-------------------------|
| Cursor            | Works                   |
| Bluetooth         | Works                   |
| Keyboard          | Works                   |
| USB Ports         | Works                   |
| WiFi              | Does not work           |
| HDMI              | Does not work           |

## Installation Guide

### Requirements
- Lenovo IdeaPad Gaming 3 with Ryzen 5 4600H and GTX 1650
- macOS installation image (e.g., Catalina or Big Sur)
- USB drive (16GB or larger)
- Access to a macOS or Hackintosh system

### Steps

1. **Download EFI Folder:**
   - Clone or download this repository.
   - Navigate to the `EFI` folder which contains the necessary OpenCore bootloader configuration.

2. **Create Bootable USB Drive:**
   - Format a USB device for installation using the Dortania guide. 

3. **Replace EFI Folder:**
   - Mount the EFI partition of the USB drive.
   - Replace the `EFI` folder on the EFI partition with the one from this repository.

4. **BIOS Settings:**
   - Disable Secure Boot.
   - Set SATA mode to AHCI.
   - Disable dGPU (Nvidia GTX 1650) in BIOS.
   - use smokeless UMAF to use integrated Radeon graphics, set to 2GB.



5. **Install macOS:**
   - Boot from the USB drive.
   - Follow the macOS installer instructions.
   - After installation, boot into macOS using the USB drive.

6. **Post-Installation:**
   - Mount the EFI partition of the installed macOS drive.
   - Replace the EFI folder on the macOS drive with the one from the USB drive.

7. **Finalize Configuration:**
   - Reboot without the USB drive.
   - macOS should now boot using OpenCore.

## Troubleshooting

- **WiFi:** Currently not supported due to incompatible hardware. Consider using a compatible USB WiFi dongle.
- **HDMI:** Currently not functional. Workarounds may involve using USB-C to HDMI adapters if supported by your laptop.
- **Graphics:** Nvidia GTX 1650 is disabled; rely on integrated graphics for display output.

##Images


![Screenshot 2024-06-30 at 3 47 01 PM](https://github.com/user-attachments/assets/7f6d82ce-188f-4b53-ac8c-abd2828226bf)

![Screenshot 2024-07-14 at 1 42 00 PM](https://github.com/user-attachments/assets/b73ad81c-c410-4f43-ab35-269d6fec4f9b)

![Screenshot 2024-07-14 at 1 41 34 PM](https://github.com/user-attachments/assets/04e8b094-d9bb-40e2-b6bf-5cc6d3b41054)



## Credits

- OpenCore Team: For the bootloader.
- Hackintosh community contributors: For various patches and configurations.
