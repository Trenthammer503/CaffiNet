# ☕ CaffiNet Chapter 1 — The Mom & Pop Infrastructure

## 📖 The Scenario

CaffiNet started as a single café run by owners **Becky and Todd Brewster**, who pride themselves on roasting beans and burning through routers with equal passion. After opening a second location, they realized their “network” is a tangled mess of old Linksys routers, USB drives labeled “important stuff,” and a shared Gmail account called CaffiNet2020backup@gmail.com.

They’ve hired **you**, their new “IT consultant,” to modernize their setup and prepare them for future growth. For now, they just want:
- A proper server
- Centralized user management
- Reliable backups
- A way for both locations to access shared files without emailing zip files named “FINAL_REALLY_FINAL_3.zip”

You’ll be working from your home lab, simulating their environment through **Proxmox**, building out a realistic small-business network that you’ll later connect to the cloud.

---

## 🎯 Mission Objective

Design and deploy CaffiNet’s **first proper on-premises infrastructure**:
- Domain Controller (Active Directory + DNS + DHCP)
- File and Print Server
- Basic VPN access for remote workers
- Automated backups
- Network documentation and topology diagram

---

## ⚙️ Constraints

- Budget-conscious owners (they *will* ask if they can pay you in coffee)
- Limited existing infrastructure (expect chaos)
- Need for scalability (future Azure expansion)
- Simulate everything in your **Proxmox lab**

---

## 🧩 Deliverables

| Deliverable | Description |
|--------------|-------------|
| Infrastructure Diagram | Diagram of CaffiNet’s initial environment |
| Server Configs | Notes and screenshots for AD, DNS, DHCP, File Server setup |
| Backup Strategy | Document outlining how data is backed up and restored |
| PowerShell Scripts | Any automation you create (user creation, backups, etc.) |
| Documentation | A written summary of how the network operates |

---

## ☕ Company Notes

- The owner’s nephew “helps with IT” and will send you unhelpful advice.  
- The coffee machines have static IPs because someone read that online.  
- Your first “ticket” will probably come from Becky asking why her printer keeps renaming itself.  

---

## ✅ Success Criteria

When this chapter is done:
- All employees authenticate via domain accounts.
- Shared drives replace manual file sharing.
- VPN users can access on-prem resources securely.
- Backups are functional and tested.
- Documentation is clear enough for someone else to maintain.

Once that’s complete, CaffiNet will begin expanding — and you’ll move into **Chapter 2: Growing Business.**

---

*“If it ain’t broke, it’s probably just not plugged in.” — Becky Brewster, CEO, CaffiNet.*
