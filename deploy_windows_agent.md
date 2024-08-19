# Run the following commands to download and install the agent:
> Requirements
>> You will need administrator privileges to perform this installation.
>> PowerShell 3.0 or greater is required.
>> Keep in mind you need to run this command in a Windows PowerShell terminal.
```powershell
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.5-1.msi -OutFile ${env.tmp}\wazuh-agent; msiexec.exe /i ${env.tmp}\wazuh-agent /q WAZUH_MANAGER='###.###.###.###' WAZUH_REGISTRATION_SERVER='###.###.###.###' 
```
# Start the agent:
```powershell
NET START WazuhSvc
```

#One-liner
```powershell
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.5-1.msi -OutFile $env:TEMP\wazuh-agent.msi; msiexec.exe /i $env:TEMP\wazuh-agent.msi /q WAZUH_MANAGER='192.168.1.20' WAZUH_REGISTRATION_SERVER='192.168.1.20'; net start WazuhSvc
```
