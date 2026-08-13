<h1 align="center">
  🔐 Project 1 — Cybersecurity Lab on Mac- Kali Linux
</h1>
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:2563EB,100:7C3AED&height=3&width=100%25" alt="divider" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Cybersecurity-0F172A?style=for-the-badge&labelColor=2563EB&logo=hackthebox&logoColor=white" alt="Cybersecurity" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-111827?style=for-the-badge&labelColor=0EA5E9&logo=kalilinux&logoColor=white" alt="Kali Linux" />
  <img src="https://img.shields.io/badge/Mac-111827?style=for-the-badge&labelColor=000000&logo=macos&logoColor=white" alt="Mac" />
  <img src="https://img.shields.io/badge/UTM-v4.6.0-111827?style=for-the-badge&labelColor=1E293B&logo=apple&logoColor=white" alt="UTM" />
  <img src="https://img.shields.io/badge/Linux-111827?style=for-the-badge&labelColor=475569&logo=linux&logoColor=white" alt="Linux" />
  <img src="https://img.shields.io/badge/Linux%20Fundamentals-111827?style=for-the-badge&labelColor=E95420&logo=linux&logoColor=white" alt="Linux Fundamentals" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-111827?style=for-the-badge&labelColor=7C3AED&logo=metasploit&logoColor=white" alt="Penetration Testing" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Cisco-111827?style=for-the-badge&labelColor=1BA0D7&logo=cisco&logoColor=white" alt="Cisco" />
  <img src="https://img.shields.io/badge/Networking-111827?style=for-the-badge&labelColor=0891B2&logo=wireguard&logoColor=white" alt="Networking" />
  <img src="https://img.shields.io/badge/Isolated%20Networking-111827?style=for-the-badge&labelColor=047857&logo=protonvpn&logoColor=white" alt="Isolated Networking" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Program-Network%20Walks-111827?style=for-the-badge&labelColor=0F766E" alt="Network Walks" />
  <img src="https://img.shields.io/badge/Instructor-Waqas%20Karim%20(CCIE)-111827?style=for-the-badge&labelColor=475569&logo=cisco&logoColor=white" alt="Waqas Karim CCIE" />
  <img src="https://img.shields.io/badge/By-Desrine%20Harripaul-111827?style=for-the-badge&labelColor=0F766E&logo=github&logoColor=white" alt="Desrine Harripaul" />
</p>
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:7C3AED,100:2563EB&height=3&width=100%25" alt="divider" />
</p>
  
# 🎯 Introduction

The purpose of this laboratory exercise is to develop the skills required to configure Kali Linux with specific configurations, as outlined by the instructor. The main difference between what was assigned and what was done is that I am using macOS, while the instructor used Windows OS. Therefore, I had to use UTM for the setup, whereas the instructor used Oracle VirtualBox.
This lab is the starting point for everything I'll build on going forward:

# 🧠 Core networking concepts

- Linux administration
- Cisco fundamentals
- Ethical hacking techniques
- Vulnerability assessment & penetration testing (VAPT)
- Home-grown security labs
- Python for security tooling
- Automating security workflows
- Andriod Setup
- Windows Setup

# 🖥️ My Setup

| Component | Details |
|---|---|
| Host Operating System | MACOS |
| Processor | Apple Silicon M1 |
| RAM | 16 GB |
| Storage | 512 GB|
| Virtualization Platform | UTM |
| Hypervisor | QEMU 10.0 |
| Guest Operating System | Kali Linux 2026.2 |
| Network Type | NAT Network Specified, However UTM equivalent for normal internet access: Shared Network |
| Subnet | 10.0.0.0/24 |
| Kali Linux IP | 10.0.0.2/24 |
| Gateway | 10.0.0.1 |
| DNS | 8.8.8.8 |

# 🔗 Files

- UTM: [https://virtualbox.org/wiki/Downloads](https://mac.getutm.app/)
- Kali Linux: https://kali.org/get-kali
- Windows iso: https://www.microsoft.com/en-us/software-download/windows11
- Andriod Studio: https://developer.android.com/studio

# Outline of steps taken

1. Download UTM
2. Setup Kali VM
3. Network: Shared Network
4. Configure Network Specifications in Kali
5. Kali VM Clone
6. Setup Windows 11 VM
7. Windows 11 Clone
8. Setup Android VM [Andriod Studio]

# 1. Download and setup UTM
   
<img width="1439" height="778" alt="Screenshot 2026-08-13 at 11 16 42 AM" src="https://github.com/user-attachments/assets/a3184df3-419f-4a24-a83e-f4034ed500f6" />



What happened: Installed UTM as the hypervisor for the whole lab.

Purpose: UTM is what lets Kali run as a fully isolated guest OS, separate from my host machine.

Outcome: ✅ Completed

# 2. Setup Kali VM

<img width="783" height="387" alt="Screenshot 2026-08-13 at 11 20 06 AM" src="https://github.com/user-attachments/assets/a3972467-8036-4ad8-92a5-0e9d1afce293" />

<img width="1184" height="900" alt="Screenshot 2026-08-13 at 11 20 42 AM" src="https://github.com/user-attachments/assets/dbeba675-100f-4b7c-b4fe-bdc96e458873" />

<img width="781" height="382" alt="Screenshot 2026-08-13 at 11 20 15 AM" src="https://github.com/user-attachments/assets/cfd51ed0-5d71-49e6-bbc9-9aecfd9ef57d" />

What happened: Downloaded Kali iso file. Configured and Deployed Kali. 

Purpose: The Kali Linux ISO provided the operating system needed for the cybersecurity lab. Configuring and deploying Kali established the virtual environment where the required network and security configurations could be performed and tested.

Outcome: ✅ Completed

# 3. Adjust Network

<img width="780" height="382" alt="Screenshot 2026-08-13 at 11 52 49 AM" src="https://github.com/user-attachments/assets/0497bdc8-1c17-4341-a34e-e82f7b75dc51" />

What happened: The network configuration for the Kali Linux virtual machine was accessed through UTM → Network Settings. The current Network Mode was set to Shared Network, which is why Kali was automatically assigned an IP address in the 192.168.64.0/24 network.

The available network modes were displayed:

- Shared Network — Kali receives a virtual network connection managed by UTM/macOS.
- Host Only — Kali can communicate with the host Mac and other appropriate virtual machines, but does not normally have direct external network access.
- Bridged (Advanced) — Kali connects to the same physical network as the Mac, appearing as another device on that network.

Purpose: The purpose was to identify the current virtual network configuration and determine the appropriate UTM network mode required to configure Kali according to the instructor's specified 10.0.0.0/24 network. This ensures that the IP configuration is compatible with the virtual network rather than simply changing the IP address and potentially losing connectivity.

Outcome: ✅ Done

# 4. Configure Network Specifications in Kali (For MAC)

What happened: 
<h3>Step 1: Open terminal and run command: ip addr</h3>
    - Verify the Interface [enp0s1 or eth0]
    <img width="1075" height="346" alt="Screenshot 2026-08-13 at 11 05 42 AM" src="https://github.com/user-attachments/assets/b3436ed3-50b3-491b-83ba-2103a742f44e" />
  
<h3>Step 2: Check your current gateway [Command: ip route]</h3>
  <img width="727" height="92" alt="Screenshot 2026-08-13 at 11 06 56 AM" src="https://github.com/user-attachments/assets/ca85fa18-998c-4a1d-ac15-e9b7f0f7552a" />

Note: <b>What this means</b>

The Kali VM is currently configured as:

- Interface: eth0
- Current IP: 192.168.64.7
- Subnet: 192.168.64.0/24
- Current gateway: 192.168.64.1
- DHCP: Yes

  <h3>Step 3: Shut down the Kali VM completely</h3>
  - Select your Kali VM.
  - Click the Settings/Edit button.
  - Go to Devices → Network (Open Advanced Settings)
<img width="786" height="388" alt="Screenshot 2026-08-13 at 12 53 22 PM" src="https://github.com/user-attachments/assets/719195e7-187d-4300-851f-81f35d8255b2" />

<b> Findings: The initial network configuration did not match the specifications provided for the laboratory exercise. Kali Linux was assigned 192.168.64.7, while UTM displayed a Guest Network of 10.0.2.0/24. This confirmed that the virtual network needed to be reconfigured to the required 10.0.0.0/24 network before proceeding with the Kali configuration. </b>

  <h3>Step 4: Adjust UTM Network Settings</h3>
        - Click inside Guest Network and change to: 10.0.0.0/24
        - Change DHCP Start: 10.0.0.15
        - Change DHCP End: 10.0.0.254
        <img width="781" height="389" alt="Screenshot 2026-08-13 at 1 06 14 PM" src="https://github.com/user-attachments/assets/69744382-450f-4b2e-8f10-cced6a94c574" />

  <h3>Step 5: Relaunch Kali</h3>
      - Open Terminal
      - Run: ip addr [Confirm the IP address]
      <img width="952" height="394" alt="Screenshot 2026-08-13 at 1 14 18 PM" src="https://github.com/user-attachments/assets/c56f49c8-9a8c-4fbb-9d98-e5abcff00718" />
     <b>Findings: The Kali VM has:
        - Interface: eth0
        - IP address: 10.0.0.16/24
        - Network: 10.0.0.0/24
        - Status: UP
So UTM is successfully giving Kali an address on the new 10.0.0.x network. Do not manually change the IP yet.</b>


  - Run: ip route [Confirm the Gateway]
      
<img width="1312" height="198" alt="image" src="https://github.com/user-attachments/assets/70b9af4c-67b0-4ea1-85db-c15434a5e98d" />

 <b>Findings: So currently:
      - Kali IP: 10.0.0.16
      - Gateway: 10.0.0.15
      - Network: 10.0.0.0/24
      - Interface: eth0
This is good because Kali is communicating with the UTM network.</b>

<h3> Step 6: Verify that the gateway is reachable</h3>
  - Run: ping -c 4 10.0.0.15
<img width="605" height="223" alt="Screenshot 2026-08-13 at 1 22 56 PM" src="https://github.com/user-attachments/assets/68be8eba-9e35-4617-aafb-7ad9e7b7aff9" />

<b>Findings: This verify that the network connection is working perfectly. ✅ </b>
Kali → eth0 → 10.0.0.16
          ↓
Gateway → 10.0.0.15
          ↓
Network working ✅

<h3>Step 7: Determine whether 10.0.0.2 is already being used before assigning it.</h3>
    - Run: ping -c 4 10.0.0.2
    <img width="1456" height="418" alt="image" src="https://github.com/user-attachments/assets/7c56fd62-00f5-4978-8e53-104b0fe09f73" />

<b> Findings: it confirms the Kali VM's networking is working, but 10.0.0.2 is not currently present on the network.</b>

  - Run: ip neigh
    <img width="1498" height="234" alt="image" src="https://github.com/user-attachments/assets/bcb69b4f-ff6a-471a-a7ad-602e5412293d" />
<b> Findings: The Kali machine is currently 10.0.0.16, and it can reach the gateway 10.0.0.15. But 10.0.0.2 does not exist/reply on the network:

10.0.0.15 → REACHABLE ✅
10.0.0.2 → FAILED ❌
The route says the gateway is 10.0.0.15.

So Kali itself is working correctly. The issue is that nothing is responding at 10.0.0.2. </b>

- Run:
  sudo ip addr flush dev eth0
  sudo ip addr add 10.0.0.2/24 dev eth0
  sudo ip link set eth0 up
  
  <img width="972" height="655" alt="Screenshot 2026-08-13 at 1 35 26 PM" src="https://github.com/user-attachments/assets/985cff7a-1623-424c-9991-7619fa9c1ea3" />

<b>Findings: So the attempt to change Kali to 10.0.0.2 did work, but DHCP is still assigning 10.0.0.16 to eth0</b>

<h3> Step 8: Configure the NetworkManager connection properly. </h3>
    - Run: nmcli connection show
    - Set the static IP: sudo nmcli connection modify "Wired connection 1" ipv4.method manual ipv4.addresses 10.0.0.2/24
    - Bring the connection down and back up:
      Run:  - sudo nmcli connection down "Wired connection 1"
            - sudo nmcli connection up "Wired connection 1"
<img width="2348" height="764" alt="image" src="https://github.com/user-attachments/assets/8d2ad2a7-3c93-45f8-8d9d-b5c5413a63ad" />
<h3> Step 9: Change the profile from DHCP to a static IPv4 configuration.</h3>
    sudo nmcli connection modify "Wired connection 1" \
    ipv4.method manual \
    ipv4.addresses 10.0.0.2/24 \
    ipv4.gateway "" \
    ipv4.dns ""
  - Then Restart the Connection: 
      - sudo nmcli connection down "Wired connection 1"
      - sudo nmcli connection up "Wired connection 1"
      
  - Then Run: ip addr show eth0 to check the IP
<img width="1250" height="721" alt="Screenshot 2026-08-13 at 2 05 40 PM" src="https://github.com/user-attachments/assets/208fbd03-d982-4ab5-b3a9-0cd9f4c2f8d8" />

Status: Success ✅

Purpose: The purpose of this configuration was to assign the Kali Linux eth0 interface a static IPv4 address of 10.0.0.2/24. Initially, the interface had both the desired 10.0.0.2 address and a secondary dynamically assigned address (10.0.0.16) obtained through DHCP. This could cause inconsistency in a networking lab where a predictable IP address is required. NetworkManager was therefore configured to use manual IPv4 configuration instead of DHCP. After restarting the connection, ip addr show eth0 was used to verify that 10.0.0.2/24 was the only IPv4 address assigned to the interface.

# 5 Kali Snapshots (Cloned)
<img width="510" height="612" alt="image" src="https://github.com/user-attachments/assets/80fd3f2c-b4c8-46e2-978a-a61927c43164" />

    
Why it mattered: If a future lab breaks something, I can roll straight back to this known-good state instead of rebuilding from scratch.

Purpose: Backup & recovery checkpoint

Outcome: ✅ Done

# 6. Windows 11 Configuration
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/45ee3406-5e30-4309-b92f-184eed594ac5" />

Why It mattered: This is the one of OS that we'll be using as a victim for Kali to hack

<b> Windows Clone:</b> <img width="530" height="750" alt="image" src="https://github.com/user-attachments/assets/f2f4b465-16b1-4ac9-90fc-7e9c1e25e6db" />

# 7. Android 

<img width="2876" height="1614" alt="image" src="https://github.com/user-attachments/assets/ac670cbe-4a93-4836-95b5-9f74efd74b59" />

<img width="792" height="1428" alt="image" src="https://github.com/user-attachments/assets/0731987d-edd2-43d1-ab6d-0f570d17fe0e" />

Why It mattered: This is the one of OS that we'll be using as a victim to Kali

# 🧠 What I learnt: 
<b> This laboratory helped me develop practical skills in Linux administration, virtualization, and network configuration. I learned how to deploy Kali Linux on an Apple Silicon Mac using UTM and QEMU, configure a virtual network, troubleshoot IP and gateway issues, and use Linux networking commands such as ip addr, ip route, ip neigh, ping, and nmcli.

I also learned the importance of understanding how DHCP, static IP addressing, gateways, and network interfaces work together. Creating snapshots taught me the value of having reliable recovery points when working in cybersecurity labs. Setting up Windows 11 and Android as additional virtual environments also provided the foundation for future vulnerability assessment and penetration-testing exercises.

Most importantly, I learned that cybersecurity is not only about using security tools; it also requires a strong understanding of operating systems, networking, virtualization, and troubleshooting.


# Copyright/Attribution 

© 2026 Desrine Harripaul. All rights reserved.

This documentation and the original laboratory work presented in this repository were created by Desrine Harripaul for educational and cybersecurity training purposes.

Third-party software, tools, logos, trademarks, and referenced resources remain the property of their respective owners. This includes Kali Linux, UTM, Apple, Cisco, Android Studio, and other referenced technologies. Their inclusion does not imply ownership or endorsement.

Where external resources, documentation, images, or materials are used, appropriate attribution should be provided to the original creators or organizations.


Week 1 setup steps complete ✅

<strong> Owned By: Desrine D. Harripaul
