# 🔧 Installation & Configuration Guide

This page documents exactly how I got this legacy IBM server up and running 

---

## 1. Operating System: Q4OS (i386)
Since the Xeon processor is 32-bit, I chose **Q4OS** because it is based on Debian and is incredibly lightweight.

### Installation Steps:
* **Tool used:** Rufus (to flash the ISO).
* **Process:** Used a USB drive to boot into the IBM BIOS (F12). 
* **Environment:** Selected the **LXDE** desktop environment to save as much of that 4GB RAM as possible.


<-- well my xeon supported both 64/32bit but i did go with 32bit cause BIOS/firmware was locked to 32bit as these are old server rigs which were based on 32bit environment (windows 7 server 32bit)-->

---

## 2. Remote Access: Webmin
Because I want to run this "headless" (no monitor), I needed a web interface.

### The Command Line Setup:
To get Webmin running on 32-bit Debian, I used these commands:

1. **Update the system:**
   `sudo apt update && sudo apt upgrade -y`

2. **Download the Webmin package:**
   `wget http://prdownloads.sourceforge.net/webadmin/webmin_2.100_all.deb`

3. **Install dependencies and the package:**
   `sudo apt install ./webmin_2.100_all.deb`

---

## 3. The "Gotchas" (Troubleshooting)
* **usr/passwd:** The user/passwd will the one you use in your machine as it is locally hosted for your machine you can just use same passwd you use in your machine.
* **The URL:** You **must** use `https://` and port `:10000`. If you use `http://`, the page will just hang.
* **Root Access:** If you get locked out, use:
  `sudo /usr/share/webmin/changepass.pl /etc/webmin root [yourpassword]`

---

## 4. Current Status
The server is currently accessible at `https://192.168.29.xxx:10000`. 
Memory usage is sitting at roughly **15%** on idle.
