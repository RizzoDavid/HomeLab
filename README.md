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
    - Quad9 for Privacy
      - 9.9.9.9
      - 149.112.112.112
  - IP Range
    - 10.1.0.1/24
  - Firewall
    - Allow Lan to Kids
    - Allow Lan to Lab
- IoT
  - Vlan 20
  - DNS
    - Quad9 for Privacy
      - 9.9.9.9
      - 149.112.112.112
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
- Dell Precision T7600 (Harry)
  - 8 Core Intel Xeon
  - 48 GB Ram
  - 500 GB SSD (sda)
  - 2 TB HDD (sdb)
  - 2 TB HDD (sdc)
  - 500 GB SSD(sdd)
  - 500 GB SSD (sde)
  - Dual Nic
  - NVIDIA Quadro K4000
- Custom PC/Server (Ron)
  - AMD Ryzen 7
    - 8 Core
  - 32 GB Ram
  - 500 GB NVME
  - 250 GB SSD
  - 1 TB HDD
  - 4 TB HDD
  - RX 580 


## Virtual Machines Running
These are the services that I am currently running. 

- XCP-NG (Harry)
  - Truenas
    - 8 GB Ram
    - 2 Cores
    - SSD Pool
      - sdd
      - sde
    - HDD Pool
      - sdb
      - sdc
    - Boot Disk
      - 20 GB
  - Home Assistant
    - 2 Cores
    - 2 GB Ram
    - 32 GB Boot
  - Jellyfin
    - 4 Cores
    - 8 GB Ram
    - 25 GB Boot
    - NVIDIA Quadro K4000
  - Lupin
    - 2 Cores
    - 4 GB Ram
    - 25 GB Boot
  - Potter
    - 4 Cores
    - 8 GB Ram
    - 25 GB Boot
  - Xen Orchestra
- XCP-NG (Ron)
  - Brother
    - 1 Core
    - 2 GB Ram
    - 20 GB Boot
  - Granger
    - 4 Cores
    - 8 GB Ram
    - 25 GB Boot
  - McGonagall
    - 2 Cores
    - 4 GB Ram
    - 25 GB Boot
  - Snape
    - 2 Cores
    - 4 GB Ram
    - 25 GB Boot
- Oracle
  - Dumbledore (Arm)
    - 1 Core
    - 6 GB Ram
    - 50 GB Boot Disk
  - Hermione (Arm)
    - 2 Cores
    - 12 GB Ram
    - 100 GB Boot Disk
  - Sirius Black (Arm)
    - 1 Core
    - 6 GB Ram
    - 50 GB Boot Disk

  