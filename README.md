# HomeLab
Here is my documentation for my homelab. I am still updating the document. Here is what this document will contain:

- Diagram of Network Topology
- Descripition of each device
- The services running
- List of hardware

## Network
- LAN
  - No VLAN
  - DNS
    - Google DNS for Speed
      - 8.8.8.8
      - 8.8.4.4
  - IP Range
    - 10.1.0.1/24
  - Firewall
    - Allow Lan to Kids
    - Allow Lan to Lab
- Kids
  - Vlan 30
  - DNS
    - OpenDNS for content filtering
      - 208.67.222.222
      - 208.67.220.220
  - IP Range
    - 10.3.0.1/24
  - Firewall
    - Block Kids to Lab
    - Block Kids to Lan
- IoT
  - Vlan 20
  - DNS
    - Google DNS For Speed
      - 8.8.8.8
      - 8.8.4.4
  - IP Range
    - 10.2.0.1/24
  - Firewall
    - Block IoT to Lan
    - Block IoT to Lab
    - Block IoT to Kids
    - Allow IoT to Chromecast
    - Allow Session IoT to Lan
    - Allow IoT to Plex
- Lab
  - Vlan 50
  - DNS
    - Windows Server DNS for Active Directory
      - 10.5.0.2
    - *.localdomain.com directed to Traefik Reverse Proxy
      - 10.5.0.5
  - IP Range
    - 10.5.0.1/24
  - Firewall
    - Allow Lab to Kids
    - Allow Lab to Lan
- BlackHole
  - Vlan 666
  - DNS
    - N/A
  - Firewall
    - No Outbound or Inbound Access
    - Device Isolation
  

## Hardware
- Unifi Security Gateway
- 16 Port Managed Switch
- 2 Unifi Access Points
- Dell Precision T7600
  - 8 Core Intel Xeon
  - 40 GB Ram
  - 20 GB SSD
  - 250 GB SSD
  - 2 TB HDD
  - 1 TB HDD
  - 1 TB HDD
  - Dual Nic
  - NVIDIA Quadro K4000
- Custom PC/Server
  - AMD Ryzen 7
    - 8 Core
  - 32 GB Ram
  - 500 GB NVME
  - 500 GB SSD
  - 500 GB SSD
  - 2 TB HDD
  - RX 580 


## Services Running
These are the services that I am currently running. 

- VMWare ESXI
  - Traefik
  - Portainer
  - VS Code Server
  - Uptime Kuma
  - TrueNas
  - 
- Windows Serer 2022
  - Active Directory
  - DNS
  - Web Server (IIS)
  - Windows Update Services
  - Windows Deployment Services


## Set Up Notes

Potential Services That I want to install
- Windows Server 2022
  - Active Directory
  - DHCP
  - DNS
  - Active Directory Federation Service 
  - Network Policy Server
  - Plex
  - Hyper-V Server
  - Web Server (IIS)
  - Windows Server Update Services
  - Remote Desktop Services
  - Windows Deployment Services
- VMWARE ESXi
  - Ubuntu 
    - Docker
      - Traefik Reverse Proxy
      - Visual Studio Code Server
      - Portainer
      - Uptime Kuma
  - Ubuntu 
    - Grafana Loki
  - TrueNas


  