Home Lab Setup

This repository documents my personal home lab setup, designed to simulate a small enterprise environment and experiment with networking, virtualization, and self-hosted services.

## Network Topology ##

The lab consists of:

- **ISP Router** – Provides Internet connectivity.
- **L2 Switch** – Connecting all devices, with VLAN-based segmentation:
  - VLAN 10 – Personal PC
  - VLAN 20 – Laptop
  - VLAN 30 – ProxMox Server
  - VLAN 40 – IoT devices
  
This segmentation improves security, isolates traffic, and simulates small enterprise network practices.

<img width="649" height="711" alt="HomeLab Diagram" src="https://github.com/user-attachments/assets/b4f0ca3c-9d3d-4d10-b1fc-cfd41e6fd729" />


## Core Infrastructure ##

### Proxmox VE Server ###
- Acts as the central virtualization platform.
- Hosts multiple **virtual machines** and **Docker containers** for various services:
  - Media servers
  - Automation scripts
  - Testing environments
  - Backups
- Lightweight scripts for managing and automating repetitive tasks.

### Raspberry Pi 5 ###
- Hosts a **private cloud** using **NextCloud** for personal storage.
- Provides **secure remote access** via **Tailscale VPN**.
- Runs lightweight services and experimental setups without affecting main infrastructure.

### Client Devices ###
- Personal PC for testing, development, monitoring and some gaming 😎.
- Laptop for work.

## Services & Tools ##
- **Networking:** VLAN segmentation, basic inter-VLAN routing (via router), service isolation.
- **Virtualization:** Proxmox VMs and LXC containers.
- **Automation:** Mini scripts for backups, service management, and monitoring.
- **Private Cloud:** Nextcloud + Tailscale VPN on Raspberry Pi for remote access.
- **Monitoring & Testing:** Occasional network monitoring, testing new services safely in isolated VLANs.

## Goals & Learning Outcomes ##
- Hands-on experience with network segmentation and infrastructure isolation.
- Practical knowledge of virtualization, containerization, and service orchestration.
- Secure remote access management using VPNs.
- Ability to simulate enterprise-style network setups in a home environment.
