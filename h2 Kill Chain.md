# h2 Kill Chain

---

# x) Cyber Kill Chain Summary

1. **Introduction**

   - Traditional methods of network defense are not enough to stop Advanced Persistent Threats (APTs).
   - APTs are well-funded and skilled attackers who target specific organizations for long periods of time.
   - They use a variety of tactics to gain access to networks, including socially-engineered emails, malware, and zero-day exploits.

2. **Related Work**

   - The kill chain is a series of steps that an attacker must follow to achieve their goal.
   - By understanding the kill chain, defenders can develop targeted defenses to stop attacks at any stage.

3. **Intelligence-Driven Computer Network Defense (CND)**

   - Intelligence-driven CND is a risk management strategy that focuses on understanding the attacker's threat component.
   - It involves analyzing adversaries, their capabilities, objectives, and limitations.
   - By studying intrusions and identifying patterns, defenders can develop more effective defenses.

3.1 **Indicators and the Indicator Lifecycle**

   - Indicators are pieces of information that can be used to identify an intrusion.
   - There are three types of indicators:
     - **Atomic**: Remains their value mostly and cannot be broken into pieces, e.g., email addresses, IP addresses.
     - **Computed**: Derived data, usually from an incident, e.g., hash values, regex.
     - **Behavioral**: Collection on Computed and Atomic indicators.
   - By tracking indicators over time, defenders can learn more about the attacker's tactics and procedures.

3.2 **Intrusion Kill Chain**

   - The intrusion kill chain is a seven-step process that attackers follow to compromise a network:
     1. **Reconnaissance**: Gather intel from where to breach, identify and select targets, gather email addresses, gain intel of technology.
     2. **Weaponization**: Creating remote access and executable code that will gain backdoor access.
     3. **Delivery**: Moving weapon to target environment, e.g., email with a PDF attachment.
     4. **Exploitation**: Triggering hacker's code in target environment.
     5. **Installation**: Gaining remote access.
     6. **Command and Control (C2)**: Hacker has "hands on access to keyboard."
     7. **Actions on Objectives**: Now hacker can work toward its goals, e.g., data exfiltration.
   - By understanding the kill chain, defenders can develop targeted defenses to disrupt the attacker's progress at any stage.

3.3 **Courses of Action**

   - Defenders can use a variety of techniques to stop attacks:
     1. **Detect**: Detect using network analytics or firewall analytics.
     2. **Deny**: Deny access from certain IPs.
     3. **Disrupt**: Disrupt attacker.
     4. **Degrade**: Degrade attacker.
     5. **Deceive**: Deceive attacker.
     6. **Destroy**: Destroy information.
   - By understanding the attacker's kill chain, defenders can choose the most effective course of action for each stage.

3.4 **Intrusion Reconstruction**

   - Analyzing past intrusions can help defenders identify patterns and develop more effective defenses.
   - It is important to reconstruct the entire kill chain, even for unsuccessful attacks.

3.5 **Campaign Analysis**

   - By analyzing multiple intrusion attempts from the same APT, defenders can identify commonalities and patterns.
   - This information can be used to develop more effective defenses and understand the attacker's intent.

4. **Case Study**

   4.1 **Intrusion Attempt 1**

   - Infected PDF that used shellcode to create a backdoor and send data to hacker server.
   - PDF was a copy of a legitimate one.

   4.2 **Intrusion Attempt 2**

   - Infected PDF that used shellcode to create a backdoor and send data to hacker server.
   - PDF was a copy of a legitimate one.
   - Sender IP address was different from the one before, but the same exploit was used.

   4.3 **Intrusion Attempt 3**

   - Noticed because of an indicator overlap (same IP as in intrusion attempt 2).
   - PowerPoint file was the infected file this time.
   - Zero-day exploit; the exploit was not known by Microsoft or anyone else.

5. **Summary**

   - Intelligence-driven CND is a necessary component of effective network defense.
   - By understanding the attacker's kill chain and using indicators to identify and track intrusions, defenders can develop more effective defenses and protect their networks from attacks.

- **Question/Insight**:
  - Given that this paper was published in 2011, how can the Cyber Kill Chain framework be adapted or updated to remain effective against modern cyber threats, including advancements in AI, machine learning, and quantum computing?

### Source
- Lockheed Martin Corporation. "Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains." [https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)

---

# a) Bookworm

## Technical Report: Installing Debian 12-Bookworm on VirtualBox for Windows

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
  
![Screenshot 2024-08-28 000437](https://github.com/user-attachments/assets/031ee528-2cf6-4929-a7d8-459d8a1781be)

2. **Create a New VM**:
   - Click `Machine` in the top menu and select `New...`.

![Screenshot 2024-08-28 000551](https://github.com/user-attachments/assets/446b29eb-9bec-4c50-a451-ce9832300017)
  
   - Change to ExpertMode!
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

---

# b) Voluntary Bonus

# Instruction: Updating All Software on Your Linux Box Using `apt-get`

## Introduction
This guide will show you how to update all software on a Linux system using the `apt-get` package manager. The instructions are intended for Debian-based distributions like Ubuntu and Debian.

## Step-by-Step Instructions

1. **Open the Terminal**:
   - Launch your terminal application, either from the application menu or by pressing `Ctrl + Alt + T`.
  
![Screenshot 2024-08-30 143828](https://github.com/user-attachments/assets/9a4c8d61-b891-4195-b109-7949439d8a27)


2. **Update the Package List**:
   - Update the list of available packages and their versions by running:
     ```bash
     sudo apt-get update
     ```
   - Enter your password when prompted.

![Screenshot 2024-08-30 144608 kopie](https://github.com/user-attachments/assets/97dcd42e-1c1f-40b8-b2d2-17d26b667b16)

3. **Upgrade Installed Packages**:
   - Upgrade all installed software to the latest versions with:
     ```bash
     sudo apt-get upgrade
     ```
![Screenshot 2024-08-30 144608](https://github.com/user-attachments/assets/a276fa8e-bb2b-4dd2-ae23-6d1100449c9b)

4. **Full Upgrade (Optional but Recommended)**:
   - For a comprehensive upgrade that handles dependencies, run:
     ```bash
     sudo apt-get dist-upgrade
     ```
![Screenshot 2024-08-30 144721](https://github.com/user-attachments/assets/8ad373f9-60a9-4f7a-a2cd-7a6aa8da36d6)

### Source
[Why you Need apt-get update and apt-get upgrade](https://blog.packagecloud.io/you-need-apt-get-update-and-apt-get-upgrade/) - Blog.Packagecloud.io

