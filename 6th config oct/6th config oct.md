---

How Ansible Works:
 
 Configuration Management server in the case of the Ansible is called as Ansible Control Node which can be any linux, unix or mac instance.
On all the NOdes Python should be installed 

Ansible uses python to do configuration management on the nodes
* Now we would ask ansible to execute playbook, Now Ansible will do the following
* Generate a Python script that installs the apache
* Copy the script to web1, web2 and web3
* Execute the script on web1, web2 and web3
* Wait for the script to complete and show the results

playbook: in this we have to create yaml file
inventory: where configuration management has to be executed
configure: we have configure ansible

Simple: Ansible was designed to have a simple setup process & minimum learning curve

ssh: ssh is a secure shell to connect linux machine

Install these below:
Ansible Control Node:
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible -y
ansible --version 

In node1:
ssh -i .\ansible.pem ubuntu@public ip
python3 --version

Now we will configure b/w this 2: password authentication:
sudo nano /etc/ssh/sshd_config
and pa yes
Ctrl x 
yes
enter
sudo service sshd restart
exit
do this on other node also

 we would create an ansible user which simulates it admin on both the machines:
Log in to nodes and execute:
anc
sudo adduser ansible
user: ansible
password: ansible
Y
su ansible
password: ansible
sudo apt update
sudo visudo
ansible ALL=(ALL:ALL) NOPASSWD:ALL  # WHEN WE EXECUTE THIS COMMANDS DONT ASK FOR PASSWORDS
su ansible
password:ansible
sudo apt update 
exit
exit

another one :
ssh -i .\ansible.pem ubuntu@publicip
sudo adduser ansible
password:
sudo visudo
ansible ALL=(ALL:ALL) NOPASSWD: ALL
su ansible
password:ansible
sudo apt update
exit
exit

on 2 missions we have admin user i.e., called as ansible

powershell/windows Terminal








anotherway:
sudo -i 
apt-get update 
apt-get install ansible -y 
visudo 
ansible
cd /etc/ansible/
ls
cd hosts
vi hosts
exit


sudo -i 
apt-get update 
apt-get install python -y 
visudo
vi /etc/ssh/sshd_config
systemctl restart sshd
su ansible
cd ~
exit










