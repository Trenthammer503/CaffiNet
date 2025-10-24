# 🏠 Home Server – Proxmox Host (Dell Precision 7810)

## 📌 Overview
A powerful home lab virtualization server designed for Proxmox VE, running tiered storage for efficiency, reliability, and learning. Supports VMs, Docker workloads, Plex, Nextcloud, cloud projects, and future CoffeeCo infrastructure.

---

## 🖥️ Hardware Summary

| Component | Details |
|-----------|---------|
| **Model** | Dell Precision 7810 |
| **CPU** | 2 × Intel Xeon E5-2630 v3 (16 cores / 32 threads total) |
| **Clock** | 2.4 GHz base / ~3.2 GHz turbo |
| **RAM** | 128GB DDR4 ECC (error-correcting, server-grade) |
| **GPU** | Installed (unused currently — available for future hardware transcoding) |
| **BIOS Storage Mode** | AHCI (for ZFS support) |

---

## 📦 Storage Architecture (Tiered)

| Tier | Device | Capacity | Purpose |
|-------|---------|----------|---------|
| **Tier 0** | 1TB SATA SSD (2.5") | 1TB | Proxmox OS + ISOs + templates |
| **Tier 1** | NVMe (PCIe adapter) | 1TB | Fast datastore for VMs, containers, and app data |
| **Tier 2** | 2 × 4TB Seagate IronWolf (NAS, CMR) | 4TB usable (ZFS mirror) | Bulk storage — Plex media, Nextcloud data, backups |

---

## 🗄️ ZFS Mirror (Tier 2) Settings

| Setting | Value |
|---------|-------|
| RAID Level | Mirror (2-disk) |
| Compression | `lz4` |
| atime | `off` |
| xattr | `sa` |
| ashift | `12` |
| autotrim | `on` |

**Use Cases:**  
- Plex media library  
- Cloud storage (Nextcloud)  
- VM/container backup targets  
- Long-term, resilient bulk storage  

---

## 🌐 Networking

| Feature | Status |
|---------|--------|
| Onboard NIC | Primary network interface |
| Dual-NIC PCIe card | Available for future projects (pfSense, VLANs, multi-network CoffeeCo scenarios) |

---

## ✅ Capabilities & Workloads

This host comfortably supports:

- Proxmox virtualization
- Docker/Portainer stack
- Plex 4K streaming
- Nextcloud
- Vaultwarden, Overseerr, Immich, etc.
- CoffeeCo project VMs and internal services
- Snapshots, backups, monitoring (Grafana + Prometheus)
- Future Kubernetes experimentation
- VPN access (WireGuard or OpenVPN)

---

## 📌 TL;DR

**Dual-Xeon / 128GB ECC Proxmox hypervisor** with **tiered storage**:  
- `1TB NVMe` → fast VMs/containers  
- `1TB SSD` → OS and utilities  
- `4TB IronWolf ZFS mirror` → resilient bulk storage

A learning-focused, enterprise-style setup with room to scale.

---
