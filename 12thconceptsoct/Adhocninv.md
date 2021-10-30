---
-v : verbose
-vv : somemore verbose
-vvv : more verbose

ssh absuible@ public ip
cd apache/
ls
ansible-playbook -i inventory apache.yml
ansible-playbook -i inventory -v apache.yml
ansible-playbook -i inventory -vvv apache.yml
ansible-playbook -i inventory -vvvv apache.yml

ls
ls -al ~
sudo apt install tree
cd ~/.ansible/
tree
cat hosts
ansible -m ping all
tree
cd /etc/ansible/
ls
tree
cat hosts
ansible -m ping all #ansible is correct or not
ansible -v -m ping all
ansible -vv -m ping all
ls -al
sudo vi ansible.cfg # all ansible commands are here
exit

ssh ansible@34.221.165.163
whereis ansible
cd /etc/ansible/
ls
ls -al
cd /usr/bin/
ls -al
ls -al | more # more info here
ls
exit

Adhoc Command: # this is onetime activity this is reboot command
From ansible we can run modules, This module is expressed as yaml and we use it tasks or handler section which leads to playbook.

ansible -i inventory -m ping all #-i inventory
#-m name of module
#all basically we want to run
ansible -m ping all # it will take default inventory
ansible -b -m 'apt' -a 'name=git update_cache=yes state=present' all 
git --version # git will present
ansible -b -m 'apt' -a 'name=git update_cache=yes state=absent' all
git --version # git will not present
ls
cd apache/
ls
cat inventory
ansible -b -i inventory -m reboot all
ansible -i inventory -m ping all

Inventory in Ansible:
ssh ansible@34.220.111.124
cd test
vi hosts #giving inventories
ansible -i hosts -m ping all
ansible -i hosts -m ping webserver
ansible -i hosts -m ping ubuntu
exit

# this is static inventory





