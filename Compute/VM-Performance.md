#  Troubleshooting VM Performance Issues  
### **Issue:** VM is slow or unresponsive.  

 **Possible Causes:**  
- High CPU or memory utilization.  
- Storage disk performance bottlenecks.  
- Network congestion affecting VM responsiveness.  
- Improper VM sizing or outdated configurations.  

 **Troubleshooting Steps:**  
 **Check VM Metrics:**  
Use Azure Monitor → Insights → Performance → CPU & Memory utilization.  

 **Analyze Disk Performance:**  
Run `df -h` (Linux) or `Get-PhysicalDisk` (PowerShell) to check disk usage.  

 **Optimize VM Sizing:**  
Use Azure Advisor recommendations for VM resizing.  

 **Check Network Latency:**  
Run `ping <destination-IP>` and `tracert <destination-IP>` to diagnose latency.  

 **Common Fixes:**  
- Resize VM to a larger SKU using **Azure Portal or CLI**.  
- Upgrade disk type to **Premium SSD for better IOPS**.  
- Adjust **NIC settings** to enhance network throughput.  
- Use **autoscaling** to balance workload demands.  
