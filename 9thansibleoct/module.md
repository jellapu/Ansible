---
ssh ansible@52.37.81.115
ls
cd apache/
vi apache.yml #add format
ansible-playbook --help
ansible-playbook --syntax-check apache.yml
ansible-playbook -i inventory --syntax-check apache.yml
ansible-playbook -i inventory apache.yml
ansible-playbook -i inventory apache.yml
exit

Handlers:
In ansible when we want to execute some tasks as a reaction to other tasks we need to use handlers.
If the module is executes handler will not get cal, when module not exwcuted handler will give call

ssh ansible@52.37.81.115
cd apache/
vi apache.yml 
ansible-playbook --syntax-check apache.yml
ansible-playbook -i inventory --syntax-check apache.yml
ansible-playbook -i inventory apache.yml
exit
