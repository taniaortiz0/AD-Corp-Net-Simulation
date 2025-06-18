## Run Commands on Windows

---

- dsa.msc : Directory Service Administration. This tool is used to manage Active Directory Users and Computers (ADUC).
- gpmc.msc : Group Policy Management Console (GPMC). The tool is used to manage Group Policy Objects (GPOs)
- wf.msc : Windows Defender Firewall with Advanced Security. It used to configure firewall rules on a Windows machine.
- gpedit.msc : Local Group Policy Editor. This tool lets you view and configure Group Policy settings on a local Windows computer.
- services.msc : Services console in Windows. This lets you view, start stop, pause, resume or configure the startup type of Windows services. 
- wsus.msc:  Opens the WSUS administration console.
  
---
## Updates 

- gpupdate /force : Forces the Group Policy to update on the client machine to ensure it's using the latest WSUS settings.
- wuauclt /detectnow: Forces the client machine to immediately check for updates from the WSUS server. 

---
