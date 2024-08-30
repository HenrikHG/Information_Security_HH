# Technical Report: Installing Debian 12-Bookworm on VirtualBox for Windows

**Note**: If you are using macOS or Linux, please refer to [this article](https://terokarvinen.com/2021/install-debian-on-virtualbox/) for platform-specific instructions.

## Introduction
This report details the installation of Debian 12-Bookworm Linux in a VirtualBox virtual machine (VM) on a Windows host machine. The guide is designed to be repeatable, allowing another person to follow along and achieve the same outcome.

## Prerequisites

### VirtualBox Installation
1. **Download VirtualBox**: 
   - Visit the [official VirtualBox website](https://www.virtualbox.org/).
   - Navigate to the [downloads section](https://www.virtualbox.org/wiki/Downloads).
   - Select the Windows host installer.
   - Download and run the installer.

2. **Install VirtualBox**:
   - After downloading, double-click the installer to launch it.
   - Follow the on-screen instructions, accepting the default settings throughout the installation process.
   - Once the installation is complete, launch VirtualBox to ensure it installed correctly.

   **Screenshot Placeholder 1**: *VirtualBox installation screen on Windows*


### Download Debian 12-Bookworm ISO
1. **Download the ISO Image**:
   - Go to the official [Debian CD Image website](https://www.debian.org/CD/live/).
   - Locate and download the latest Debian 12-Bookworm live ISO. The specific file as of this writing is `debian-live-12.6.0-amd64-xfce.iso`.
   - Save the ISO file to a convenient location on your computer.

   **Screenshot Placeholder 2**: *Debian 12-Bookworm download page*

## Creating a New Virtual Machine

### Step-by-Step Instructions

1. **Launch VirtualBox**:
   - Open VirtualBox on your Windows machine.

2. **Create a New VM**:
   - Click `Machine` in the top menu and select `New...`.
   - Fill in the following details:
     - **Name**: DebianBookworm
     - **Type**: Linux
     - **Version**: Debian (64-bit)
   - Allocate **Memory Size** to 4096 MB (4 GB) or more, depending on your system's RAM.
   - Choose `Create a virtual hard disk now` and click `Create`.

   **Screenshot Placeholder 3**: *VirtualBox New VM settings on Windows*

3. **Configure Virtual Hard Disk**:
   - Select `VDI (VirtualBox Disk Image)` as the hard disk file type.
   - Choose `Dynamically allocated` storage.
   - Set the **file size** to 60 GB, then click `Create`.

   **Screenshot Placeholder 4**: *Virtual Hard Disk configuration screen*

4. **Insert Debian ISO Image as a Virtual CDROM**:
   - With your new VM selected, click `Settings`.
   - Navigate to the `Storage` tab.
   - Under `Controller: IDE`, select the `Empty` CDROM drive.
   - On the right side, click the CD icon next to `Optical Drive`.
   - Select `Choose a disk file...` and browse to the Debian ISO you downloaded earlier.
   - Click `OK` to close the settings window.

   **Screenshot Placeholder 5**: *ISO image selection in VirtualBox*

## Booting and Installing Debian 12-Bookworm

1. **Boot the Virtual Machine**:
   - In the VirtualBox Manager, double-click your newly created VM to start it.
   - The VM will boot from the Debian ISO, bringing up the Debian boot menu.

2. **Start the Debian Installer**:
   - In the boot menu, select `Graphical Install` and press `Enter`.

   **Screenshot Placeholder 6**: *Debian boot menu*

3. **Configure Installation**:
   - Follow the on-screen instructions to configure the installation.
   - Select your preferred language, location, and keyboard layout.
   - Configure the network settings if required, and set up the root password and user account.

   **Screenshot Placeholder 7**: *Debian installer language selection*

4. **Partition Disks**:
   - Select `Guided - use entire disk` for partitioning.
   - Choose `All files in one partition (recommended for new users)` and continue.

   **Screenshot Placeholder 8**: *Partition disk setup*

5. **Finish Installation**:
   - After partitioning, the installer will copy files to the virtual hard disk.
   - When prompted, install the GRUB boot loader. Choose the default device.
   - Finish the installation and reboot the VM when asked.

   **Screenshot Placeholder 9**: *Installation progress screen*

6. **First Boot into Debian**:
   - After rebooting, the VM will boot into your newly installed Debian 12-Bookworm system.
   - Log in using the user account created during installation.

   **Screenshot Placeholder 10**: *Debian login screen*

## Conclusion
This guide provides detailed instructions for installing Debian 12-Bookworm on VirtualBox using a Windows host machine. The process was straightforward, and the virtual environment functioned as expected. Following these steps, anyone should be able to replicate the setup and start using Debian within VirtualBox.

**Note**: Screenshots will be added later to support the visual understanding of the instructions.
