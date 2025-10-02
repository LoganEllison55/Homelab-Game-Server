# Homelab-Game-Server
This project showcases my self-built home lab server used to host Minecraft and other game servers for friends and family. The setup highlights both hardware and software skills, including system deployment, network tunneling, remote administration, and automated backups.

---

## Project Overview

I repurposed an **HP EliteDesk 705 G4** into a dedicated Ubuntu-based server. After upgrading with a **256 GB NVMe SSD** and **16 GB of additional RAM** (24 GB total), I installed **Ubuntu Server** for stability and security, and configured it for **headless operation** with SSH.  

For game hosting, I deployed the **AMP (CubeCoders)** panel to provision and manage Minecraft servers and used **Playit.gg tunneling** to securely expose the server to external players without revealing my home IP. To ensure reliability, I implemented automated backup schedules with pruning policies, along with manual restore validation.

---

## Key Features

- Built a dedicated home server from repurposed hardware (HP EliteDesk 705 G4).  
- Installed **Ubuntu Server** and configured **OpenSSH** for encrypted remote access.  
- Added **Webmin** for web-based system monitoring and management.  
- Deployed **AMP (CubeCoders)** to manage Minecraft servers and other game instances.  
- Provisioned a Minecraft Java & Bedrock instance, allocated memory, installed mods, and granted operator privileges.  
- Enabled secure public access using **Playit.gg tunneling** to mask IP and manage port forwarding.  
- Configured **automated daily backups** and restore testing for uptime and integrity.  
- Performed hardware prep and maintenance (thermal paste replacement, additional RAM and storage along with, BIOS validation).  

---

## Technologies Used

- **Operating System:** Ubuntu Server  
- **Remote Access:** OpenSSH, Webmin  
- **Game Server Management:** AMP (CubeCoders)  
- **Networking & Security:** Playit.gg tunneling, port mapping  
- **Backup & Recovery:** AMP scheduled tasks, Webmin backup policies  
- **Hardware:** HP EliteDesk 705 G4, NVMe SSD, DDR4 RAM upgrade  

---

## Common Issue & Resolution

**Issue:**  
Friends could not connect to the Minecraft server after setup, even though the game instance was running correctly.  

**Root Cause:**  
The issue was traced to network exposure — AMP had provisioned the Minecraft instance locally, but the server was not reachable from outside the home network due to NAT/firewall restrictions.  

**Resolution:**  
1. Verified that the Minecraft server was bound to the correct port (25565) within AMP.  
2. Installed and configured **Playit.gg**, which creates a secure tunnel and provides a public hostname for players.  
3. Shared the Playit.gg hostname with friends, who were then able to connect successfully without requiring manual router port forwarding or exposing the home IP.  

This demonstrated the importance of secure tunneling for hobbyist game servers hosted on residential ISPs.

---

## Project Learnings

- Gained hands-on experience in Linux server administration and headless management.  
- Practiced troubleshooting real-world issues involving networking, NAT traversal, and port exposure.  
- Implemented practical security concepts, such as IP masking and encrypted remote access.  
- Strengthened ability to design, deploy, and maintain resilient services using both open-source and licensed software.  

---

## How to Reproduce (Simplified Steps)

1. **Prepare Hardware**  
   - Clean and test repurposed PC (HP EliteDesk 705 G4).  
   - Upgrade storage to NVMe SSD and expand RAM.  

2. **Install OS & Tools**  
   - Install **Ubuntu Server** via USB.  
   - Enable **SSH** for headless access.  
   - Install **Webmin** for web-based management.  

3. **Deploy Game Panel**  
   - Install **AMP (CubeCoders)** and apply license.  
   - Create a new Minecraft instance.  
   - Allocate RAM, configure mods, and set server operators.  

4. **Networking**  
   - Install and configure **Playit.gg** tunnel service.  
   - Map the internal Minecraft port to the external hostname.  

5. **Backups**  
   - Configure scheduled backups (daily at 10:00 UTC).  
   - Test backup restoration.  

---

## Screenshots

<img width="445" height="456" alt="Image" src="https://github.com/user-attachments/assets/137cc3cc-6a8c-437a-abab-64826e32f78a" />

<img width="979" height="513" alt="Image" src="https://github.com/user-attachments/assets/a6da9192-1a95-498d-b187-915d955eddaf" />

---

## Author

**Logan Ellison**  
Self-taught IT enthusiast | Building hands-on projects in servers, networking, and cybersecurity.  

---
