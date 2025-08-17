# Create an Azure Virtual Machine (Free Tier) – Azure Portal

## ✅ Prerequisites
- An active **Azure Free Tier** subscription
- Access to the **Azure Portal** (https://portal.azure.com)
- Free-tier eligible region (e.g., East US, West Europe)

---

## 🚀 Steps to Create a VM

### 1. Sign in
Login to the Azure Portal: https://portal.azure.com

---

### 2. Navigate to **Virtual Machines**
- In the left-hand menu, click on **“Virtual machines”**
- Click **“+ Create” → “Azure virtual machine”**

---

### 3. **Basics** Tab
| Field               | Value / Description |
|---------------------|--------------------|
| Subscription         | *Your Free Tier subscription* |
| Resource Group       | Create new or select existing |
| Virtual machine name | e.g. `myFreeVM` |
| Region               | Select a **Free services eligible region** |
| Availability options | *Leave default* |
| Image                | **Ubuntu Server 22.04 LTS** (free tier eligible) |
| Size                 | Click "See all sizes", then select **B1s** |
| Username             | Enter a username |
| Authentication type  | Password (or SSH key) |
| Inbound port rules   | Allow **SSH (port 22)** |

Click **Next** at the bottom.

---

### 4. **Disks** Tab
- OS disk type → **Standard SSD (free tier)**  
Click **Next**

---

### 5. **Networking** Tab
- Virtual network: Leave default (auto-created)
- Subnet: Leave default
- Public IP: **Enabled**
- NIC network security group: **Basic**
- Allow selected ports: **SSH (22)**

Click **Next**

---

### 6. **Management** Tab
- Monitoring → **Disable Boot diagnostics** (not free tier)
- Keep the rest as default  
Click **Next**

---

### 7. **Advanced** Tab
- Leave everything default  
Click **Next**

---

### 8. **Tags** Tab
- Optional – add tags if needed  
Click **Next**

---

### 9. **Review + Create**
- Review validation summary  
- Click **Create**

---

### ✅ After Deployment
- Go to **“Go to resource”**
- Copy the **Public IP address**
- SSH into your VM:

```bash
ssh <username>@<public-ip-address>