# HomeLab
Here is my documentation for my homelab. I am still updating the document. Here is what this document will contain:

- Diagram of Network Topology
- Descripition of each device
- The services running
- List of hardware

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


## Services Running
These are the services that I am currently running. 

- VMWare ESXI
  - Ubuntu Server
    - Docker
    - Portainer
    - VS Code Server
    - Traefik Reverse Proxy
  - Windows Server 2022
    - Active Directory
    - DNS
    - File and Storage Services
    - Plex
  - TrueNas
  - Kemp Load Balancer
    - 3 Load Balanced Ubuntu VMs running Docker
    - Ubuntu VM Running Ansible
  - Windows 10 VM
  - Ubuntu VM 
    - Docker for Penetration Testing