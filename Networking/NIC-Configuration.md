#  Troubleshooting NIC Configuration Issues  
### **Issue:** VM cannot connect due to NIC misconfiguration.  

 **Possible Causes:**  
- Incorrect **IP address or subnet settings**.  
- Misconfigured **NSG or firewall rules**.  
- NIC is not properly associated with VM.  
- Public IP disassociation preventing external connectivity.  

 **Troubleshooting Steps:**  
**Check NIC Settings:**  
Run `ifconfig` (Linux) or `Get-NetAdapter` (PowerShell).  

 **Verify IP Assignment:**  
Use `az network nic list-ip-configs`.  

 **Test Network Connectivity:**  
Ping gateway and external sites to check response time.  

 **Common Fixes:**  
- Assign a new **static IP** or reconfigure **DHCP settings**.  
- Update **NSG and firewall rules** in Azure Portal.  
- Reassociate NIC with VM via **Azure CLI** or portal.  
