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
| Client crashed because of 3D acceleration `VBoxManage modifyvm "DC01" --accelerate3d on`  | VBoxVGA controller doesn't support 3D acceleration  | Changed controller to `vmsvga`  |
| Windows Server 2025 didn't work on VM  | VM showed "No bootable medium found" but ISO was properly attached  | I switched to Windows Server 2022 instead  | 
| GUI in VirtualBox and other apps (Obsidian) didn't work properly on Arch Linux | `xdg-desktop-portal` issues - the service that handles file dialogs and app integration was broken  | Workaround - configured everything via CLI (`VBoxManage`) instead of GUI  |

## What I've learned
- Creating users, groups and OU
- Resetting passwords
- Block accounts
  
