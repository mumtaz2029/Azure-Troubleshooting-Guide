# 🛠️ Troubleshooting VM Disk Issues  
### **Issue:** VM disk is full, inaccessible, or slow.  

🔹 **Possible Causes:**  
- Insufficient disk space.  
- Unoptimized disk caching or performance tier.  
- Incorrect permissions blocking access.  
- Unhealthy disk due to high IOPS usage.  

🔹 **Troubleshooting Steps:**  
✅ **Check Disk Space:**  
Run `df -h` (Linux) or `Get-Volume` (PowerShell).  

✅ **Verify Disk Health:**  
Monitor metrics via **Azure Portal → Disks → Performance**.  

✅ **Review Storage Configuration:**  
Ensure disk is attached properly using `lsblk` (Linux) or `Get-Disk` (PowerShell).  

🔹 **Common Fixes:**  
- Expand disk storage via Azure **Resize Disk** feature.  
- Switch to **Premium SSD** for better IOPS performance.  
- Correct permissions using `chmod` (Linux) or **RBAC policies**.
  
