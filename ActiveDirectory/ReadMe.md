# Active Directory HomeLab

## Project objective
To learn ActiveDirectory for Helpdesk role, I created HomeLab with Windows Server 2022 (DC01) and Client with Windows 10 (Client01)  

## Environment
- Arch Linux + VirtualBox
- Windows Server 2022 (DC01)
- Windows 10 Pro (CLIENT01)

## What I've done

1. Created NAT network (192.168.100.0/24)
2. Installed Windows Server 2022 on VM (DC01)
3. Set static IP (192.168.100.10) i DNS (127.0.0.1)
4. Installed Active Directory and promoted server to domain controller
5. Installed Windows 10 Pro on VM (CLIENT01)

## Issues and Troubleshooting
| Issue | What was wrong | How it was fixed |
|:------------|:------------|:-----------------|
| No ping between VMs  | Server had two cards with same IP `192.168.100.10`  | Network Card 2 (NAT) set to DHCP, Card 1 static  |

<img width="956" height="775" alt="screenshot_20260611_141518" src="https://github.com/user-attachments/assets/5000054a-a0af-43f6-865b-fa374395e697" />
<img width="407" height="456" alt="screenshot_20260611_141459" src="https://github.com/user-attachments/assets/4665b054-3170-417b-9780-d17ea63b7851" />
<img width="1030" height="812" alt="screenshot_20260611_140954" src="https://github.com/user-attachments/assets/be753d0f-b9be-4233-921e-55945520564a" />



| Issue | What was wrong | How it was fixed |
|:------------|:------------|:-----------------|
| Client crashed because of 3D acceleration `VBoxManage modifyvm "DC01" --accelerate3d on`  | VBoxVGA controller doesn't support 3D acceleration  | Changed controller to `vmsvga`  |
| Windows Server 2025 didn't work on VM  | GUI metod failed for unknown reason | Used PowerShell instead: `Add-Computer -DomainName "adlab.local" -Credential ADLAB\Administrator -Restart`  | 
| Couldn't join Client01 via GUI  | VM showed "No bootable medium found" but ISO was properly attached  | I switched to Windows Server 2022 instead  | 
| GUI in VirtualBox and other apps (Obsidian) didn't work properly on Arch Linux | `xdg-desktop-portal` issues - the service that handles file dialogs and app integration was broken  | Workaround - configured everything via CLI (`VBoxManage`) instead of GUI  |  

<img width="959" height="1040" alt="screenshot_20260524_172545" src="https://github.com/user-attachments/assets/064ea479-e8c3-4835-bc9d-fed8883e829e" />


## What I've learned
- Creating users, groups and OU
- Resetting passwords
- Block accounts

  <img width="958" height="800" alt="screenshot_20260526_222636" src="https://github.com/user-attachments/assets/566c8479-d480-4f61-9efc-964546f23e0c" />

  <img width="957" height="785" alt="screenshot_20260526_222718" src="https://github.com/user-attachments/assets/884017db-f947-468a-a2b9-6ff1e7798b52" />

