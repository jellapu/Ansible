---
cd C:\Users\JYO\Downloads\
ssh ansible@54.202.154.164
ansible --version
mkdir test
cd test/
vi hosts
172.31.21.78
ls
ansible -i hosts -m ping --ask-pass all #ansible -i <inventory file path> -m ping --ask-pass all
SSH password:ansible
vi hosts
172.31.21.78
localhost
ansible -i hosts -m ping --ask-pass all
SSH password:ansible
exit

ssh -i .\ansible6.pem ubuntu@54.202.154.164 # for this it didnt ask password

usng key for automation In this key pair try to copy the public key from ans to node1 with respect to private key
public and private keys will coincide 
ssh-keygen
ls ~/ssh/
ssh-copy-id ansible@ip node1 private
password:
now we are in ans private ip
ssh node1 private
exit  # when we do this it will shows ans private ip
cd test/
ls
cat hosts
ansible -i hosts -m ping all
ssh-copy-id ansible@localhost
ansible -i hosts -m ping all
ls ~/.ssh/
exit

Creting centos7:
ssh -i .\ansible@public ip of centos 7
python3 --version
python --version
sudo vi /etc/ssh/sshd_config
password authentication :yes
sudo service sshd restart
sudo adduser ansible
sudo passwd ansible
asking 2 times password
sudo visudo
ansible ALL=(ALL) NoPASSWD: ALL
exit


ssh ansible@ans ip
password:
exit
ssh ansible@ans private
password
ssh-copy-id ansible@node2 ip private
ssh node2 ip private
exit
cd test/
vi hosts
172.31.21.78
localhost
172.31.44.207
ansible -m ping -i hosts all
exit
























