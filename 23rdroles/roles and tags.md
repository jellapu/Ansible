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


cd .\role-structure\
tree -f


defaults
handlers
files
tasks
templates

import or include can be applied to places, handlers, tasks
import is static and include is dynamic

Tags:
In Ansible we can add tags to a single task or include statement

  1st priority : commands
  2nd priority : host
  3rd proirity : group
  4th : vars files
  5th : tasks