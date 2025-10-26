# 🏠 Homelab Overview

Welcome to my personal **homelab documentation** — a living record of my local infrastructure, services, and network organization.  
Everything here runs inside **Proxmox VE (Atlas)** on my internal LAN.

---

## 🌐 Network Summary

| Hostname | Purpose | LAN IP | Notes |
|-----------|----------|--------|-------|
| `pve-atlas` | Proxmox Virtual Environment host | `192.168.1.242` | Primary hypervisor managing all VMs and containers |
| `pihole` | Pi-hole DNS + Ad-blocking server | `192.168.1.100` | Handles LAN DNS queries and blocks ads network-wide |

---

## 🧠 Current Services

| Service | Hosted On | Description |
|----------|------------|-------------|
| **Proxmox VE** | Bare metal (`pve-atlas`) | Type-1 hypervisor managing VMs, storage, and networking |
| **Pi-hole** | Debian VM | DNS sinkhole + ad-blocker; will become network-wide once router swap is complete |
| **Unbound (planned)** | Debian VM (with Pi-hole) | Local recursive DNS resolver for privacy and speed |
| **ASUS Router (incoming)** | — | Will serve as main router with Pi-hole as upstream DNS |
