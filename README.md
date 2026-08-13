# networkwalks-B082-Week1-Cybersecurity-Lab-Setup

<h1 align="center">🔐 Building My First Cybersecurity Lab</h1> <p align="center"> <img src="https://img.shields.io/badge/Cybersecurity-0F172A?style=for-the-badge&labelColor=2563EB&logo=kalilinux&logoColor=white" alt="Cybersecurity" /> <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-111827?style=for-the-badge&labelColor=0EA5E9&logo=kalilinux&logoColor=white" alt="Kali Linux" /> <img src="https://img.shields.io/badge/VirtualBox-v7.2.14-111827?style=for-the-badge&labelColor=2563EB&logo=virtualbox&logoColor=white" alt="VirtualBox" /> <img src="https://img.shields.io/badge/Linux-111827?style=for-the-badge&labelColor=475569&logo=linux&logoColor=white" alt="Linux" /> <img src="https://img.shields.io/badge/Networking-111827?style=for-the-badge&labelColor=0891B2" alt="Networking" /> <img src="https://img.shields.io/badge/Penetration%20Testing-111827?style=for-the-badge&labelColor=7C3AED&logo=kalilinux&logoColor=white" alt="Penetration Testing" /> <img src="https://img.shields.io/badge/Program-Network%20Walks-111827?style=for-the-badge&labelColor=0891B2" alt="Network Walks" /> <img src="https://img.shields.io/badge/Instructor-Waqas%20Karim%20(CCIE)-111827?style=for-the-badge&labelColor=475569" alt="Waqas Karim CCIE" /> <img src="https://img.shields.io/badge/By-%5BYour%20Name%5D-111827?style=for-the-badge&labelColor=0F766E&logo=github&logoColor=white" alt="Desrine Harripaul" /> </p> <p align="center"> 
  
  <strong>Network Walks Cybersecurity Program — Week 1 Lab</strong> </p> <p align="center"> VirtualBox • Kali Linux • Isolated Networking • Linux Fundamentals </p>
  
# 🎯 Introduction

The purpose of this laboratory exercise is to develop the skills required to configure Kali Linux with specific configurations, as outlined by the instructor. The main difference between what was assigned and what was done is that I am using macOS, while the instructor used Windows OS. Therefore, I had to use UTM for the setup, whereas the instructor used Oracle VirtualBox.
This lab is the starting point for everything I'll build on going forward:
--------------------------------------------------------------------------------------------------------------------------------------------
# Core networking concepts

-> Linux administration
-> Cisco fundamentals
-> Ethical hacking techniques
-> Vulnerability assessment & penetration testing (VAPT)
-> Home-grown security labs
-> Python for security tooling
-> Automating security workflows
--------------------------------------------------------------------------------------------------------------------------------------------

# 🖥️ My Setup

Component	Details
Host OS	MACOS
CPU	M1
RAM	16GB
Storage	512GB
Virtualization Software	UTM
Hypervisor	QEMU 10.0
VM Architecture	ARM64 / AArch64
Guest OS	Kali Linux
Network Mode	NAT Network Specified, However UTM equivalent for normal internet access: Shared Network
Subnet	10.0.0.0/24
Kali IP	10.0.0.2/24
Gateway	10.0.0.1
DNS	8.8.8.8
--------------------------------------------------------------------------------------------------------------------------------------------

# 🔗 Files

VirtualBox: [https://virtualbox.org/wiki/Downloads](https://mac.getutm.app/)
Kali Linux: https://kali.org/get-kali
--------------------------------------------------------------------------------------------------------------------------------------------

Outline of steps taken

1. Download UTM
2. Setup Kali VM
3. Network: Shared Network
4. Configure Network Specifications in Kali
5. VM Snapshots
--------------------------------------------------------------------------------------------------------------------------------------------

1. Download and setup UTM
   
<img width="1439" height="778" alt="Screenshot 2026-08-13 at 11 16 42 AM" src="https://github.com/user-attachments/assets/a3184df3-419f-4a24-a83e-f4034ed500f6" />


What happened: Installed UTM as the hypervisor for the whole lab.

Purpose: UTM is what lets Kali run as a fully isolated guest OS, separate from my host machine.

Outcome: ✅ Completed
--------------------------------------------------------------------------------------------------------------------------------------------
2. Setup Kali VM

<img width="783" height="387" alt="Screenshot 2026-08-13 at 11 20 06 AM" src="https://github.com/user-attachments/assets/a3972467-8036-4ad8-92a5-0e9d1afce293" />

<img width="1184" height="900" alt="Screenshot 2026-08-13 at 11 20 42 AM" src="https://github.com/user-attachments/assets/dbeba675-100f-4b7c-b4fe-bdc96e458873" />

<img width="781" height="382" alt="Screenshot 2026-08-13 at 11 20 15 AM" src="https://github.com/user-attachments/assets/cfd51ed0-5d71-49e6-bbc9-9aecfd9ef57d" />

What happened: Downloaded Kali iso file. Configured and Deployed Kali. 

Purpose: The Kali Linux ISO provided the operating system needed for the cybersecurity lab. Configuring and deploying Kali established the virtual environment where the required network and security configurations could be performed and tested.

--------------------------------------------------------------------------------------------------------------------------------------------

text
Network Type : NAT Network
CIDR         : 10.0.0.0/24
DHCP         : Enabled

Outcome: ✅ Done

<!-- Add your own screenshots here -->
4️⃣ Bringing Kali Online

What happened: Downloaded the Kali Linux VM, imported it into VirtualBox, and attached it to the NAT Network I'd just built.

Why it mattered: Kali is the actual workbench — the OS I'll run tools, scans, and exercises from for the rest of the program.

text
OS            : Kali Linux
Version       : 2026.2
Hypervisor    : Oracle VirtualBox
Network       : NatNetwork

Outcome: ✅ Done

<!-- Add your own screenshots here -->
5️⃣ Giving Kali an Identity on the Network

What happened: Set a static-style IP, gateway, and DNS on Kali's network interface.

Why it mattered: Without correct addressing, Kali can't reach the gateway or resolve DNS — basic connectivity has to work before anything else does.

text
IP Address : 10.0.0.2/24
Gateway    : 10.0.0.1
DNS        : 8.8.8.8

Commands I ran:

bash
ifconfig
sudo ifconfig eth0 down
sudo ifconfig eth0 up
ping google.com

Outcome: ✅ Done

<!-- Add your own screenshots here -->
6️⃣ Locking In a Snapshot

What happened: Took a VirtualBox snapshot right after finishing the base configuration.

Why it mattered: If a future lab breaks something, I can roll straight back to this known-good state instead of rebuilding from scratch.

Purpose: Backup & recovery checkpoint

Outcome: ✅ Done

<!-- Add your own screenshots here -->
🎥 Demo
<!-- Link your own demo video here -->

📹 Demo Video: [Add your video link]

🏗️ How It All Fits Together
text
Host Machine
     │
     ▼
Oracle VirtualBox
     │
     ▼
NAT Network (10.0.0.0/24)
     │
     ▼
Kali Linux VM (10.0.0.2/24)
     │
     ▼
Future Security Labs
🧠 What I Took Away From This
Deploying and configuring a virtual machine from scratch
Setting up an isolated NAT network in VirtualBox
Installing and configuring Kali Linux
IPv4 addressing and subnetting in practice
Verifying connectivity and troubleshooting network interfaces
Using snapshots as a safety net before experimenting
🔐 Ground Rules

This lab exists strictly for learning and authorized practice. Every technique I try here stays inside systems and networks I own or have explicit permission to test — nothing in this repo is meant for use against systems you don't control.

👨‍🏫 Credit

Built as part of the Network Walks cybersecurity program, under the guidance of Waqas Karim (CCIE). Thanks for the mentorship through this first phase.

📊 Status

6 / 6 setup steps complete ✅

Learn it. Break it. Fix it. Secure it.

Network Walks Cybersecurity Program — Week 1
