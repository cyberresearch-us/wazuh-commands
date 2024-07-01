# Run the following commands to download and install the agent:
## Requirements
## You will need administrator privileges to perform this installation.
## Shell Bash is required.
## Keep in mind you need to run this command in a Shell Bash terminal.

wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.7.5-1_amd64.deb && sudo WAZUH_MANAGER='###.###.###.###' dpkg -i ./wazuh-agent_4.7.5-1_amd64.deb

# Start the agent:
sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
