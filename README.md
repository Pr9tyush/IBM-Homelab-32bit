# IBM-Homelab-32bit
legacy 32-bit server into a modern NAS.
# 🖥️ My IBM Xeon Server
**A 32-bit Home-Lab**

---

### 📌 The Project
It was a old server for loacal business i brought it. Its a "2007 IBM Intel Xeon system X3200 M2" server i repurposed it as my personal NAS 

### 🛠️ Hardware & OS
* **Server:** IBM Legacy (Xeon Processor)
* **RAM:** 4GB (DDR2)
* **Storage:** 512gb HDD's (2) 
* **OS:** Q4OS (Debian-based) + LXDE
* **Control Center:** Webmin (Port 10000)

---

### ✅ Progress Log
- [x] Flashed Q4OS to the server.
- [x] Installed Webmin for remote browser access.
- [x] Set up the port from 10000 - xxxxx (cannot be scaned easily)
- [x] Setup Samba for mobile file sharing 

---

### 💡 Why Webmin?
Since CasaOS/ZimaOS need 64-bit Docker, I used Webmin as a lightweight dashboard. It lets me manage files and hardware from my phone without needing a monitor and my pc is too old to process things it i control it via my phone and cpu idle is very low and ram is also low cause its running LXDE enviroment on it leading to less resource usage on it. And i used 512gb not 1tb or 2tb cause its my first project NAS will do more.
