---
In Ansible control node:
cd C:\Users\JYO\Downloads\
ssh -i .\ansible6.pem ubuntu@35.85.56.223
yes
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
ansible --version
exit

In Node1:
ssh -i .\ansible6.pem ubuntu@34.218.245.202
yes
python --version
python3 --version
exit

In Ansible control node:
ssh -i .\ansible6.pem ubuntu@35.85.56.223
sudo service sshd restart
exit

In node1:
ssh -i .\ansible6.pem ubuntu@35.85.56.223
sudo adduser ansible
type 2 times password
Y
su ansible
cs ~
sudo apt update
password:
exit
su ansible
sudo apt update
exit
exit

ssh -i .\ansible6.pem ubuntu@34.218.245.202
sudo adduser ansible
type 2 times password
Y
sudo visudo
su ansible
sudo apt update
exit
exit



