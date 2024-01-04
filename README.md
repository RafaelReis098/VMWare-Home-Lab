# VMWare-Home-Lab
Documenting My Cybersecurity Home lab Journey: Building for Detection &amp; Monitoring

# Cybersecurity Homelab Journey: Building for Detection & Monitoring

## Introduction

Greetings fellow enthusiasts! I'm documenting my journey of setting up a Cybersecurity Homelab to enhance my skills in detection and monitoring. This detailed account will provide insights into each step, covering the challenges and triumphs along the way.

### What is a Homelab?

A Homelab is a dedicated environment within your home for practicing and honing skills in a specific field. Think of it as a miniaturized version of large-scale infrastructures, providing a secure space to experiment and learn.

## Content

### Building The Host PC

For this lab, I've chosen a PC with the following specifications:

- **CPU:** AMD Ryzen 5 3600X 3.8 GHz 6-Core Processor
- **RAM:** G.Skill Ripjaws V Series 32 GB (2 x 16 GB) DDR4 Memory
- **STORAGE:** Crucial P1 1TB M.2-2280 NVME SSD
- **GRAPHICS CARD:** MSI GeForce GT 710 2 GB Video Card
- **MOTHERBOARD:** Asus TUF GAMING X570 ATX Motherboard
- **HOST OPERATING SYSTEM:** Windows 10 Pro

[Check out the PC build tutorial here.](insert link)

Feel free to use a dedicated server or an old laptop if it meets the VM requirements (8GB RAM minimum, preferably 16GB).

### Downloading & Installing VMware Workstation Pro

I've opted for VMware Workstation 16 Pro as my hypervisor for this lab. While it comes with a $120 price tag, it's a worthwhile investment. Alternatively, VirtualBox is a free and feature-rich alternative from Oracle.

[Watch the VMware Workstation installation tutorial here.](insert link)

### Configuring pfSense

pfSense will serve as our firewall, ensuring network segmentation and security. I've downloaded the pfSense ISO file and configured it with the following steps:

- Create a new Virtual Machine in VMware Workstation.
- Rename the VM to "pfSense" and allocate 20GB disk space.
- Customize hardware settings: Increase memory to 2GB and add 5 network adapters.
- Follow on-screen prompts for pfSense configuration.

This marks the end of the initial pfSense setup; the rest will be configured through the Kali machine using WebConfigurator.

... (continue formatting the rest of the content)

## Conclusion

Congratulations! You've reached the end of this comprehensive Cybersecurity Homelab setup. It's been an exciting journey, and you now possess the knowledge and tools to experiment, research, and enhance your skills. Feel free to explore detection rules, SIEM content, rule tuning, and even devise attack scenarios to further hone your expertise. I'll continue to update and expand on this lab, ensuring it remains detailed and up-to-date. Happy labbing!

