# ☕ CoffeeCo — Chapter 1 Mission Briefing  
### “The Mom & Pop Infrastructure”

---

## 🎬 Scenario Recap

You’ve been contracted by **CoffeeCo**, a two-location café that’s outgrown its “everything runs off Becky’s laptop” IT model.  
The owners, **Becky and Todd Brewster**, need a simple, reliable **on-prem environment** to unify their users, data, and printers.  

Their nephew “knows computers” but recently bricked the router trying to *port-forward the printer*. You’re stepping into the aftermath.

---

## 🗺️ Project Overview

**Goal:** Build CoffeeCo’s first production-style IT backbone in your **Proxmox lab**, mirroring what a real small business would need.

You’ll:

1. Stand up a **Proxmox host** and create an isolated lab network.  
2. Deploy a **Windows Server 2022 Domain Controller** (AD + DNS + DHCP).  
3. Add a **File Server VM** with basic shares and permissions.  
4. Configure **local DNS, DHCP scopes, static reservations**, and an internal domain (e.g., `coffeeco.local`).  
5. Simulate 3-5 client workstations using lightweight VMs or nested instances.  
6. Implement a **basic backup** routine (to another Proxmox storage or NAS share).  
7. Document everything — diagrams, credentials template, and setup notes.

---

## 🧩 Quest List — Fast Projects That Feed the Main Goal

| Quest | Objective | Deliverable |
|:--|:--|:--|
| ☕ Q1 | **Build the Lab** | Working Proxmox host with virtual switch & storage pool |
| 🖥️ Q2 | **Deploy DC01** | AD + DNS + DHCP configured; domain = `coffeeco.local` |
| 📁 Q3 | **Deploy FS01** | Shared folder structure (`Finance`, `POS`, `Marketing`) with permissions |
| 🔐 Q4 | **User Provisioning** | PowerShell script to bulk-create users & groups |
| 🔄 Q5 | **Backup & Recovery** | Nightly snapshot or Veeam-style backup documented |
| 🗺️ Q6 | **Diagram & Docs** | Updated `Diagram.png`, `BuildNotes.md`, `Server-Inventory.md` |

Each quest stands alone — complete them in order or bounce around as time allows.

---

## 🧠 Learning Focus for Week 1

### 1️⃣ Proxmox Foundation
- Install latest Proxmox VE ISO.  
- Create bridge (`vmbr0`) for lab VMs.  
- Configure storage pools (local-lvm or NFS/SMB).  
- Snapshot the base install.

### 2️⃣ Windows Server Deployment
- Create VM: 4 GB RAM, 2 vCPU, 60 GB disk.  
- Mount Windows Server 2022 ISO; install and patch.  
- Assign static IP → configure DNS.  
- Rename host to **DC01** and promote to Domain Controller.  
- Create first domain admin account `COFFEECO\Admin-Chris`.

### 3️⃣ Documentation Starts Now
- Begin `BuildNotes.md` — log every decision, command, and IP.  
- Update `Server-Inventory.md` with hostname, IP, roles, OS build.  
- Rough-sketch your network diagram (Visio, draw.io, Lucidchart, etc.).  

---

## 🪜 Week-by-Week Roadmap (Phase 1 Mini-Arc)

| Week | Focus | Milestone |
|:--|:--|:--|
| 1 | Lab setup + DC01 deployment | Domain online |
| 2 | FS01 + shared folders + permissions | Staff can map drives |
| 3 | DHCP tuning + VPN gateway simulation | Remote connectivity |
| 4 | Backup testing + documentation polish | Chapter 1 complete |

When Chapter 1 closes, you’ll have a **fully functional on-prem SMB environment** — the same setup many consultants charge for.

---

## 🧾 Deliverables Checklist

- [ ] `Diagram.png` updated and committed  
- [ ] Domain Controller operational  
- [ ] File Server + shares with NTFS permissions  
- [ ] User creation script (committed under `/Scripts/powershell/`)  
- [ ] Backups verified and documented  
- [ ] `Summary.md` written (what you learned, issues encountered)

---

## ☕ Owner Message (Flavor Text)

> *“Hey Chris, Todd says the Wi-Fi printer keeps printing empty pages every time someone microwaves soup. We’re thinking maybe that’s related? Anyway, can you get that new ‘server thing’ going soon? The accountant says our invoices are living in three different Google Drives.”*  
> — **Becky Brewster**, CEO, CoffeeCo (and Chief Microwave Officer)

---
