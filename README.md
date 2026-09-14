# MD102-Hybrid-Lab - Endpoint Administrator Lab
Brampton, ON | MD-102 Prep - HP Laptop Hyper-V Lab

## Why 3 VMs? Hybrid Identity for MD-102

- **DC01**: Windows Server 2022 - Forest `brampton.local` / `lab.com`
AD DS, DNS installed via `Install-ADDSForest`
Created OU `Brampton Users`, User `harpreet@brampton.local`
Proves: AD Forest, Users, Domain Admin

- **CLIENT01**: Windows 11 Domain Joined to brampton.local
Tested `brampton.local\harpreet` login, `whoami`, GPO
Proves: Domain Join, On-Prem to Hybrid concept

- **WIN-AUTOPILOT**: Windows 11 Workgroup for Pure Cloud Autopilot
Local user `LabAdmin` - Hardware hash exported
Proves: Cloud-Native, Autopilot, Intune ready

## Proof of Work

### 1. Hyper-V - All 3 VMs for Hybrid Lab
![Hyper-V Lab](Screenshot%202026-09-14%20130212.png)

### 2. WIN-AUTOPILOT Desktop - LabAdmin Ready
![Autopilot Desktop](Screenshot%202026-09-14%20130547.png)

### 3. Autopilot HWID - C:\AutopilotHWID.csv 9KB
![HWID Export](Screenshot%202026-09-14%20131552.png)
`Get-WindowsAutopilotInfo -OutputFile C:\AutopilotHWID.csv` - 9/13/2026

## Commands Used
`Install-ADDSForest -DomainName brampton.local`
`New-ADUser -Name "Harpreet Singh"` / `dsa.msc` GUI
`Get-WindowsAutopilotInfo`

Skills: AD DS Forest | DNS | AD Users/OU | Hybrid Join | Autopilot | Hyper-V | PowerShell
