---
At ansible_server_:
ssh -i .\ansible_key.pem ubuntu@35.86.164.27 #ansible user
sudo -i 
adduser ansible
visudo #sudo permissions
vi /etc/ssh/sshd_config #ssh permissions
systemctl restart ssh #service restart
su ansible
exit
apt-get update #For updating
apt-get install ansible -y
ansible --version

ssh -i .\ansible_key.pem ubuntu@35.86.164.27
sudo -i
su ansible
cd ~
ssh-keygen
ssh-copy-id ansible@172.31.25.165
ssh ansible@172.31.25.165
vi inventory/hosts #or sudo vi inventory/hosts
ssh-copy-id ansible@localhost
ssh-copy-id ansible@172.31.18.77
ssh-copy-id ansible@localhost
ssh-copy-id ansible@172.31.18.77
ssh-keygen
ssh-copy-id ansible@172.31.18.77
rm .ssh/known_hosts
ssh-copy-id ansible@172.31.18.77
mkdir test
sudo vi /test/host
cd test/
touch host
nano host
ansible -i host -m ping all
ssh-copy-id ansible@localhost
ansible -i test/host -m ping all
ssh-copy-id ansible@172.31.25.165
ansible -i test/host -m ping all


At Ubuntu_Ansible_node1:
ssh -i .\ansible_key.pem ubuntu@54.149.182.25
sudo adduser ansible
sudo vi /etc/ssh/sshd_config
sudo su ansible
exit
python --version
client_loop: send disconnect: Connection resetPS C:\Users\JYO\Downloads> ssh ansible@172.31.18.77 #DNS server
sudo -i
systemctl restart sshd
su ansible
cd ~
exit
vi /etc/ssh/sshd_config
systemctl restart ssh
exit
ssh ansible@172.31.18.77
client_loop: send disconnect: Connection reset


At centos:
ssh -i C:\Users\JYO\Downloads\ansible_key.pem  centos@ec2-54-149-65-56.us-west-2.compute.amazonaws.com
sudo -i
python3 --version
adduser ansible
passwd ansible
visudo
vi /etc/ssh//sshd_config
systemctl restart ssh
systemctl restart ssh.service
systemctl restart sshd.service
su ansible
exit









