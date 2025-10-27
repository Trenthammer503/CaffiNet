# ☕ CoffeeCo — Chapter 1 Summary  
### “The Mom & Pop Infrastructure”

**Start date:** [YYYY-MM-DD]  
**End date:** [YYYY-MM-DD]  
**Version:** 0.1

---

## 🚀 What Was Achieved
_Brief overview of the completed infrastructure build (AD, DNS, File Server, etc.)._

---

## 🔧 Key Technical Highlights
- Set up Proxmox host on hardware with bridging and storage pool.  
- Deployed Windows Server 2022 as DC01 with AD, DNS and DHCP configured.  
- Deployed File Server (FS01) with shared folders: Finance, POS, Marketing.  
- Created PowerShell user-provisioning script.  
- Implemented backup strategy and documented process.  

---

## 🧠 What I Learned
- (Example) How to configure Windows Server 2022 promotion to domain controller.  
- (Example) VLAN and virtual bridge separation in Proxmox.  
- (Example) Permissions modelling for shared folders in small business.  
- (Example) Importance of documentation (Server-Inventory.md, Diagram.png) from day one.  

---

## 😬 Challenges and How I Solved Them
- (Example) The DHCP scope overlapped with static reservations — I resolved by adjusting scope to 192.168.10.0/24 and excluding 192.168.10.1-.10.  
- (Example) The file share was slow because host disk was not using optimum storage pool — I fixed by adding a second disk and moving virtual disk to the faster pool.  
- (Example) The backup script failed due to permissions; added service account and proper rights.  

---

## 💰 Cost Reflection
- Estimated CapEx: ~$2,500 (see Budget.md)  
- Estimated OpEx: ~$250/year  
- Actual cost to me (lab use): ~$0 hardware additional + evaluation licenses = $0  
- Reflection: Using evaluation licenses and refurbished hardware drastically reduces actual cost while maintaining realistic business cost modelling — a great win.  
- Going forward: When CoffeeCo expands into hybrid cloud (Chapter 4), I expect hardware CapEx to drop and OpEx (cloud spend) to increase — giving me a chance to compare real-world “on-prem vs cloud” cost trade-offs.

---

## ✅ Next Steps
1. Prepare for Chapter 2: Growing Business — implement patching (WSUS), monitoring, helpdesk automation.  
2. Refine lab topology, add second site simulation.  
3. Update `/Documentation/IT-Costs.md` to begin aggregate cost tracking across chapters.  

---

*“If it ain’t broke… it’s probably just unplugged.” — Becky Brewster, CEO, CoffeeCo*

