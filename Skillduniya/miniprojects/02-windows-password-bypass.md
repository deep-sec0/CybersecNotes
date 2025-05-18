# Mini Project 02: Windows 7 Password Bypass Attempt (Failed – SAM Not Loaded)

## Summary

This mini project was focused on bypassing the Windows 7 login password using **Ophcrack** and rainbow tables in a virtual machine environment. The attempt failed because the **SAM and SYSTEM files from the Windows 7 VM could not be successfully accessed or loaded in Kali Linux**.

---

## Objective

- Bypass a local Windows 7 user login password
- Use **Ophcrack** on Kali Linux with rainbow tables
- Load SAM and SYSTEM files and attempt password cracking

---

## Tools & Setup

- **Kali Linux (VM)**
- **Windows 7 (VM)**
- **Ophcrack**
- **Rainbow Tables:** xp free fast version

---

## Steps Attempted

### 1. Mounting the Windows Drive in Kali
```bash
sudo mkdir /mnt/windows
sudo mount /dev/sda1 /mnt/windows

**Expected to locate:** /mnt/windows/Windows/System32/config/

But this failed. Either the Windows partition wasn’t recognized properly, or mounting the virtual drive didn’t expose the required path.

---

## Step 2: Launching Ophcrack

- Opened **Ophcrack** on Kali
- Loaded **Rainbow Tables** (`xp free fast`)
- Tried to load SAM file via:
File → Load → Encrypted SAM
❌ **SAM file could not be selected or was not visible inside the mounted path.**

---

## Result

- The Windows 7 SAM file could not be loaded into Ophcrack.
- Password cracking attempt could not proceed.
- **No access to hashes = no password cracking.**

---

## Possible Causes

- SAM file path incorrect or access permissions blocked  
- VirtualBox Guest Additions or shared folders not properly configured  
- Mounted file system was **read-only**  
- SAM file was locked because the Windows VM was active or improperly shut down

---

## Reflection

Even though the attack didn’t work, this project highlighted:

- Real-world VM and drive-mounting limitations  
- The need for proper **offline access** when targeting SAM/SYSTEM  
- How tools like **Ophcrack** rely on correct file access and structure

> **"Sometimes what fails teaches you more than what works." ✅**

