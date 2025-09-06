# Active Directory, Users, Groups, and GPO

## 1. Promote DC01
- Install **AD DS + DNS** roles  
- Promote to **Domain Controller**  
- New forest: minster.local  
📸 Screenshot: `dc-promo.png`

## 2. Create OUs, Users & Groups
- **OU Structure:**  
  - OU=Corp  
    - Users  
    - Computers  
    - Groups  
📸 Screenshot: `aduc-ous-users-groups.png`

- **Test User:** Navya Sruthi  
- **Group:** Sales Department  
- Added Navya to Sales Department  
📸 Screenshot: `aduc-ous-users-groups.png`

## 3. GPOs
- **GPO-User-Lockdown** → Hide Control Panel  
- **GPO-Wallpaper** → Set desktop wallpaper  
📸 Screenshot: `gpo-lockdown.png`  
📸 Screenshot: `gpo-wallpaper.png`
