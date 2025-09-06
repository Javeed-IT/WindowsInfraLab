# Project 1 — Core Windows Infrastructure in Azure

## A. Azure Network & VMs

- **Resource Group:** rg-infra-lab  
- **VNet:** vnet-infra-lab (10.0.0.0/16)  
- **Subnet:** subnet-workload (10.0.1.0/24)  

**Domain Controller VM:**  
- Name: DC01  
- Windows Server 2022  
- Private IP: 10.0.1.4  
- RDP allowed from my IP  
📸 Screenshot: `rg-vnet-dns.png`

**Client VM:**  
- Name: CL01  
- Windows 10/11 Pro  
- Dynamic IP  
📸 Screenshot: `cl01-domain-joined.png`

**DNS Settings:**  
- Custom DNS pointing to DC01 (10.0.1.4)  
📸 Screenshot: `rg-vnet-dns.png`