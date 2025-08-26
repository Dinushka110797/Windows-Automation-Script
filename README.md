# Windows Automation Script
Windows installation Automation Script

Windows Unattended Installation XML File
This repository contains an Autounattend.xml file for automating the installation of Windows via a USB drive. This setup is designed to skip most of the manual configuration steps, requiring you only to select the target partition.

⚠️ Important Compatibility Note
This Autounattend.xml file is configured to work ONLY with Legacy BIOS (MBR) boot mode. It will not work with UEFI (GPT).

Prerequisites
A Windows ISO file.

A USB drive (8GB or larger).

A tool to create a bootable USB (e.g., Rufus).

🚀 Quick Start Guide
1. Create Your Bootable USB Drive
Use a tool like Rufus to create a bootable Windows installation USB from your ISO file.

In Rufus, you MUST select "MBR" for the Partition Scheme to ensure compatibility with this XML file.
(If your USB is already created for UEFI (GPT), you will need to recreate it for MBR).

2. Configure Your Computer's BIOS
Before booting from the USB, you must change your boot settings:

Restart your computer and enter the BIOS/UEFI setup (usually by pressing Del, F2, F10, or Esc during startup).

Navigate to the Boot tab or settings.

Change the Boot Mode from "UEFI" to "Legacy" or "CSM" (this enables MBR support).

Save changes and exit the BIOS.

3. Add the XML File to the USB
Insert the bootable USB into your computer.

Open the USB drive.

Copy the Autounattend.xml file from this repository.

Paste it directly into the root folder of the USB drive (the main directory, alongside sources, boot, etc.).

4. Run the Automated Installation
Boot your computer from the USB drive.

The installation will start automatically.

The only step you need to interact with is selecting the partition where you want to install Windows.

Sit back, chill, and enjoy! The rest of the setup (language, region, product key, user account creation, etc.) will be handled automatically.

📁 File Contents
Autounattend.xml - The answer file that automates the Windows Setup process.

❓ Troubleshooting
Installation doesn't start automatically / asks for input: This usually means the boot mode is incorrect. Double-check that your USB was created for MBR and that your BIOS is set to Legacy/CSM mode.

File not found error: Ensure the Autounattend.xml file is placed in the root of the USB drive and not inside any folder.

Disclaimer: Use this file at your own risk. Always back up important data before performing a fresh OS installation.

