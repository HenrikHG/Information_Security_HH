# h2 Kill Chain

# Cyber Kill Chain Summary

- **Concept**: The Cyber Kill Chain, developed by Lockheed Martin, is a systematic framework that details the stages of a cyber intrusion. It provides a structured approach to understanding, detecting, analyzing, and mitigating cyber threats, particularly from Advanced Persistent Threats (APTs).

- **Phases**:
  1. **Reconnaissance**: Attackers perform research and gather intelligence on their target to identify vulnerabilities. This may include scanning networks, harvesting email addresses, or researching key personnel.
  2. **Weaponization**: The gathered information is used to create a payload, typically a piece of malware, by coupling an exploit (e.g., zero-day vulnerability) with a delivery mechanism (e.g., a phishing email).
  3. **Delivery**: The weaponized payload is transmitted to the target. Common delivery methods include spear-phishing emails, malicious websites, or infected USB drives.
  4. **Exploitation**: The delivered payload exploits a vulnerability in the target system, triggering malicious code execution. This can involve exploiting software vulnerabilities, tricking users into executing harmful files, or exploiting system features.
  5. **Installation**: Malware is installed on the victim's system, establishing a persistent presence. This step ensures that the attacker maintains long-term access to the compromised system.
  6. **Command and Control (C2)**: The compromised system establishes an outbound connection to an external server controlled by the attacker. This C2 channel allows the attacker to remotely control the system, execute commands, and exfiltrate data.
  7. **Actions on Objectives**: Having gained control of the system, the attacker performs the intended actions, such as data exfiltration, spreading to other systems, disrupting operations, or manipulating sensitive information.

- **Purpose and Benefits**:
  - The Cyber Kill Chain model assists defenders in identifying and disrupting the attack at various stages. By understanding each phase, security teams can implement specific countermeasures tailored to each stage, increasing the chances of thwarting the attack.
  - The model emphasizes that disrupting just one stage of the kill chain can prevent the attacker from achieving their objectives. This approach helps in creating a more resilient defense system.
  - It also aids in prioritizing security investments and resources, ensuring that defenses are comprehensive and capable of responding to the full spectrum of potential threats.

- **Applications**:
  - Organizations use the Cyber Kill Chain to develop intelligence-driven defense strategies. This includes mapping out potential adversary behaviors, aligning defensive measures to counter these behaviors, and continuously updating defenses based on new threat intelligence.
  - The model also serves as a framework for measuring the effectiveness of security operations. By analyzing past incidents through the kill chain lens, organizations can identify gaps in their defenses and make data-driven decisions to improve their security posture.

- **Question/Insight**: - Given that this paper was published in 2011, how can the Cyber Kill Chain framework be adapted or updated to remain effective against modern cyber threats, including advancements in AI, machine learning, and quantum computing?

# Source
- Lockheed Martin Corporation. "Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains." [https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)


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


## Conclusion
This guide provides detailed instructions for installing Debian 12-Bookworm on VirtualBox using a Windows host machine. The process was straightforward, and the virtual environment functioned as expected. Following these steps, anyone should be able to replicate the setup and start using Debian within VirtualBox.
