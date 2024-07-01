# Run the following commands to download and install the agent:
## Requirements
## You will need administrator privileges to perform this installation.
## PowerShell 3.0 or greater is required.
## Keep in mind you need to run this command in a Windows PowerShell terminal.

Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.5-1.msi -OutFile ${env.tmp}\wazuh-agent; msiexec.exe /i ${env.tmp}\wazuh-agent /q WAZUH_MANAGER='###.###.###.###' WAZUH_REGISTRATION_SERVER='###.###.###.###' 

# Start the agent:

NET START WazuhSvc
