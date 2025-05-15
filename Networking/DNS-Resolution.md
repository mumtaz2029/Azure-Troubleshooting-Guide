#  Troubleshooting DNS Resolution Issues  
### **Issue:** VM or app cannot resolve domain names.  

 **Possible Causes:**  
- Misconfigured DNS server settings.  
- Blocked DNS requests due to firewall rules.  
- Incorrect virtual network or custom DNS setup.  

 **Troubleshooting Steps:**  
 **Check DNS Configuration:**  
Run `cat /etc/resolv.conf` (Linux) or `Get-DnsClientServerAddress` (PowerShell).  

 **Test DNS Resolution:**  
Use `nslookup <domain>` or `dig <domain>` for Linux.  

 **Check NSG and Firewall Rules:**  
Verify if UDP **Port 53** is allowed.  

 **Common Fixes:**  
- Set proper **Azure-provided DNS** or custom DNS in VNet settings.  
- Allow **UDP traffic on port 53** via NSG.  
- Use **Azure DNS Resolver** for hybrid connectivity.  
