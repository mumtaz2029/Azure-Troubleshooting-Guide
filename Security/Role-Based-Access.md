# 🛡 Troubleshooting RBAC Misconfigurations  
### **Issue:** User or service lacks necessary permissions in Azure.  

 **Possible Causes:**  
- Missing or incorrect **Azure RBAC roles**.  
- Expired **service principal or identity permissions**.  
- Misconfigured access scope (Subscription, Resource Group, etc.).  

 **Troubleshooting Steps:**  
 **Check RBAC Roles:**  
Run `az role assignment list --assignee <user-email>` to verify permissions.  

 **Verify Access Scope:**  
Use **Azure Portal → IAM → Role Assignments** to confirm roles.  

 **Inspect Service Principal Status:**  
Run `az ad sp show --id <app-id>` for verification.  

 **Common Fixes:**  
- Assign correct **roles (Owner, Contributor, Reader)** using Azure CLI.  
- Extend **service principal** validity period if expired.  
- Restrict access **to specific Resource Groups** for better security.  
