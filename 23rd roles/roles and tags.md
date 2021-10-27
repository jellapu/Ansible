---
Roles: these playbook reusable in ansible and it is important also


ssh ansible@pubic ip of anc
ansible-galaxy install geerlingguy.mysql

cd mysqlusingroles
ansible-playbook -i hosts mysql.yml --syntax-check
ssh ip
sudo service mysql status
mysql -u root -P
show databases #checking for mysql
exit

ssh ansible@pubic ip of anc
pwd
ls -al
cd .ansible/
ls
cd geerlingguy.mysql/
tree

cd Ansiblezone/
cd 0ct21/
mkdir role-strucuture/
ansible-galaxy init sample
ls

