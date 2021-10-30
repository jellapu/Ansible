---
First and foremost advantage of using Jinja2 is we can avoid static file copies.


Ansible Behavioral Parameters
The list of behavior parameters
Name	Default	Description
ansible_host	Name of the host	Hostname or IP address to SSH
ansible_port	22	port to ssh to
ansible_user	root	User to SSH as
ansible_password	(None)	Password to use for SSH Authentication
ansible_ssh_private_key_file	(None)	SSH Private key to use for SSH authentication
ansible_python_interpreter	/usr/bin/python	Python interpreter on the host
ansible_connection	smart	How Ansible will connect to host