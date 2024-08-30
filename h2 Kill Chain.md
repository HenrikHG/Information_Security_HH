# Technical Report: Installing Debian 12-Bookworm on VirtualBox for Windows

**Note**: If you are using macOS or Linux, please refer to [this article](https://terokarvinen.com/2021/install-debian-on-virtualbox/) for platform-specific instructions.

## Introduction
This report details the installation of Debian 12-Bookworm Linux in a VirtualBox virtual machine (VM) on a Windows host machine. The guide is designed to be repeatable, allowing another person to follow along and achieve the same outcome.

## Prerequisites

### VirtualBox Installation
1. **Download VirtualBox**: 
   - Visit the [official VirtualBox website](https://www.virtualbox.org/) and navigate to the [downloads section](https://www.virtualbox.org/wiki/Downloads).
   - Select the Windows host installer.
   - Download and run the installer.

2. **Install VirtualBox**:
   - After downloading, double-click the installer to launch it.
   - Follow the on-screen instructions, accepting the default settings throughout the installation process.

![Screenshot 2024-08-28 002816](https://github.com/user-attachments/assets/e89bf1b0-bce5-465c-ad6e-d8117eff4b64)

![Screenshot 2024-08-28 003031](https://github.com/user-attachments/assets/4cad2de6-6197-4ee1-a762-bcadadfe7250)


   - Once the installation is complete, launch VirtualBox to ensure it installed correctly.

![Screenshot 2024-08-28 000437](https://github.com/user-attachments/assets/214f8d4a-3735-4db5-ae1b-99201a7f71f0)


### Download Debian 12-Bookworm ISO
1. **Download the ISO Image**:
   - Go to the official [Debian CD Image website](https://www.debian.org/CD/live/).
   - Locate and download the latest Debian 12-Bookworm live ISO. The specific file as of this writing is `debian-live-12.6.0-amd64-xfce.iso` OR click this [DOWNLOAD LINK](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/debian-live-12.6.0-amd64-xfce.iso)
   - Save the ISO file to a convenient location on your computer.
  
## Creating a New Virtual Machine

### Step-by-Step Instructions

1. **Launch VirtualBox**:
   - Open VirtualBox on your Windows machine.

2. **Create a New VM**:
   - Click `Machine` in the top menu and select `New...`.
   - Change to ExpertMode

![Screenshot 2024-08-28 000551](https://github.com/user-attachments/assets/446b29eb-9bec-4c50-a451-ce9832300017)

   - Fill in the following details:
     - **Name**: DebianBookworm
     - **Type**: Linux
     - **Version**: Debian (64-bit)
   - Select `Choose a disk file...` and browse to the Debian ISO you downloaded earlier.
   - Skip `unattended install`

![Screenshot 2024-08-28 000652](https://github.com/user-attachments/assets/abe2e0d0-e25f-4273-9f1c-7c9cd7bf4963)

   - Allocate **Memory Size** to 4096 MB (4 GB) or more, depending on your system's RAM.

![Screenshot 2024-08-28 000758](https://github.com/user-attachments/assets/baa2cf64-4b72-4e83-87cb-13527c950654)

   - Create a Virtual Hard Disk
   - Set the **file size** to 30 GB.

![Screenshot 2024-08-28 000823](https://github.com/user-attachments/assets/e45cc2a0-e77e-4737-a1b9-8c1a6c08d070)

   - Click on `Finish`

## Booting and Installing Debian 12-Bookworm

1. **Boot the Virtual Machine**:
   - In the VirtualBox Manager, double-click your newly created VM to start it.
   - The VM will boot from the Debian ISO, bringing up the Debian boot menu.

![Screenshot 2024-08-28 001008](https://github.com/user-attachments/assets/9338e5c7-d456-4e54-b380-94afc9779bac)

2. **Start the Debian Installer**:
   - In the boot menu, select `LIve install` and press `Enter`.

![Screenshot 2024-08-28 001106](https://github.com/user-attachments/assets/2e05b400-0c96-4d13-8ed8-32dcca2f62b7)

3. **First Boot into Debian**:
   - After rebooting, the VM will boot into your newly installed Debian 12-Bookworm system.

![Screenshot 2024-08-28 001324](https://github.com/user-attachments/assets/2d51625a-94c3-482f-934d-a96d1e5ddf85)

4. **Test the system**:
    - You may want to open the Browser to test the connection
  
![Screenshot 2024-08-28 001418](https://github.com/user-attachments/assets/f4335465-3117-403c-9a5d-aff8069dc370)


## Conclusion
This guide provides detailed instructions for installing Debian 12-Bookworm on VirtualBox using a Windows host machine. The process was straightforward, and the virtual environment functioned as expected. Following these steps, anyone should be able to replicate the setup and start using Debian within VirtualBox.
