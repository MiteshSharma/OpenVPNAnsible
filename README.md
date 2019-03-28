# OpenVPN server and client setup using Ansible

This is an Ansible project which is used to set up OpenVPN server on ubuntu instance. We need to provide IP address of this instance with port 22 open as ansible internally uses SSH to do the setup. In this project, we first setup OpenVPN on instance and then create client ovpn file which is downloaded locally so we can use it with VPN client tool. You need to have ansible installed on your local machine from where you are running these commands. 

This project has two ansible roles:

1. openVPNServer role: To create OpenVPN server setup
2. openVPNClient role: To create OpenVPN client ovpn file


You can change variables for openVPNClient role so you can create ovpn files with different users.

playbook.yml is main ansible file which is executed by ansible command.

Steps to execute this project:
1. Clone this project on your local machine
2. Start your ubuntu instance with port 22 open to be accessed from your local machine
3. Update inventory file with correct IP address of an ubuntu instance
4. Execute Ansible command mentioned below:

Ansible command: **ansible-playbook playbook.yml**

More information about ansible can be found [here](https://www.ansible.com/).
