# VMWare-Home-Lab
Documenting My Cybersecurity Home lab Journey: Building for Detection &amp; Monitoring

# Cybersecurity Homelab Journey: Building for Detection & Monitoring

## Introduction

I'm documenting my journey of setting up a Cybersecurity Homelab to enhance my skills in detection and monitoring. This detailed account will provide insights into each step, covering the challenges and triumphs along the way.

### What is a Homelab?

A Homelab is a dedicated environment within your home for practicing and honing skills in a specific field. Think of it as a miniaturized version of large-scale infrastructures, providing a secure space to experiment and learn.

## Content

### Building The Host PC

For this lab, I've chosen a PC with the following specifications:

- **CPU:** AMD Ryzen 5 5600X 3.7 GHz 6-Core Processor
- **RAM:** Silicon Power Value Gaming 32 GB (2 x 16 GB) DDR4 Memory
- **STORAGE:** TEAMGROUP 1TB M.2-2280 NVME SSD
- **GRAPHICS CARD:** ASROCK Radeon RX 6600 8 GB Video Card
- **MOTHERBOARD:** GIGABYTE B550M AORUS ELITE ATX Motherboard
- **HOST OPERATING SYSTEM:** Windows 11 Pro

I didn't feel like using a dedicated server or an old laptop beacsue the ones I had did not meet the VM requirements (8GB RAM minimum, preferably 16GB).

### Downloading & Installing VMware Workstation Pro

I've opted for VMware Workstation 17 (Non-Commercial) as my hypervisor for this lab. Alternatively, I could have used VirtualBox because it is a free and feature-rich alternative from Oracle, but I heard it has a reputation for crashing.

I followed the instructions of the following video to set up the project
[Watch the VMware Workstation installation tutorial here.](https://www.youtube.com/watch?v=gp5eXjWZUBk&ab_channel=CYBERWOX)

### Configuring pfSense

pfSense will serve as the firewall, ensuring network segmentation and security. I've downloaded the pfSense ISO file and configured it with the following steps:

- Create a new Virtual Machine in VMware Workstation.
- Rename the VM to "pfSense" and allocate 20GB disk space.
- Customize hardware settings: Increase memory to 2GB and add 5 network adapters.
- Follow on-screen prompts for pfSense configuration.

I followed the instructions of the following video to set up the pfsense machine
[Watch the pfSense installation tutorial here.]((https://www.youtube.com/watch?v=68k1zF2jOJ4&ab_channel=CYBERWOX))

This is the end of the initial pfSense setup; the rest will be configured through the Kali machine using WebConfigurator.

### Configuring Security Onion

Security Onion takes center stage as our all-in-one IDS, Security Monitoring, and Log Management solution. The configuration involves downloading the Security Onion ISO file, installing it with specific settings, and setting up the management and monitor interfaces.

I had some trouble with this one becasue I had to install a seperate machine to use the Security Onion web interface. The OS on the new machine was Ubuntu. 
The problem I ran into was that I thought I could run the web interface with the Security Onion machine not running, but that caused it to not want to work 
when I opened the Ubuntu machine. Then I realized that I could open multiple windows with VMWare (Free) and then open and use multiple machines at one time.
This solved the problem and I could use the Web Interface on the Ubuntu machine.

I followed the instructions of the following video to set up the Security Onion and Ubuntu
[Follow the Security Onion setup steps here.]((https://www.youtube.com/watch?v=68k1zF2jOJ4&ab_channel=CYBERWOX))

### Configuring Kali Linux

Kali Linux will be the designated attack machine for various offensive actions. The setup involves downloading the Kali Linux ISO and configuring the VM with specific network settings. Just added another NAT on the system and routed it to VMnet2. 

I followed the instructions of the following video to set up the Kali Linux machine
[Download and set up Kali Linux with these steps.](https://www.youtube.com/watch?v=i0j-6iFBozg&ab_channel=CYBERWOX)

### Configuring Windows Server as a Domain Controller

Our Windows Server will play the role of a Domain Controller, part of an Active Directory domain. The setup includes downloading the Windows 2019 Server Evaluation Copy and configuring the server with specific settings.

[Follow the steps for configuring Windows Server here.](https://www.youtube.com/watch?v=lwxNGUIEB2A&ab_channel=CYBERWOX)

### Configuring Windows 10 Desktop & Adding a User to the AD Domain

This phase involves adding two Windows 10 desktops to the domain, creating users, and ensuring connectivity. Steps include downloading the Windows 10 Evaluation Copy and configuring the desktops as per The Cyber Mentor's Active Directory Hacking Lab guide.

[Set up Windows 10 and join PCs to the domain with these instructions.](https://www.youtube.com/watch?v=VmQDzjq_e_g&ab_channel=CYBERWOX)

### Installing Splunk on a Ubuntu Server

Splunk, a widely used SIEM, takes the stage for log aggregation and correlation. The installation involves setting up a Ubuntu Server, downloading Splunk, and configuring it on port 8000.

[Install and configure Splunk with this step-by-step guide.](https://www.youtube.com/watch?v=ia9E4x8iVDk&ab_channel=CYBERWOX)

### Installing Universal Forwarder on Windows Server

To forward logs to Splunk, the universal forwarder is installed on the Windows Server. Configuration steps include adding network adapters to Splunk, setting up receiving on the Splunk server, and installing the universal forwarder on Windows Server.

[Set up the Universal Forwarder and configure Splunk receiving with these instructions.](https://www.youtube.com/watch?v=yP_PFRy-pdA&ab_channel=CYBERWOX)





