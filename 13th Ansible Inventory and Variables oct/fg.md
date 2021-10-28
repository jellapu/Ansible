---
Ansible Inventory:
ssh ansible@34.214.4.177
cd test/
cat
 hosts
ansible -i hosts -m ping all
ansible -i hosts -m setup all
ansible -i hosts -m setup all >ubuntu.json
vi ubuntu.json # will observe what connect io nodes and ip addresses
ansible -m setup -a 'filter=*os*' all
ansible -i hosts -m setup -a 'filter=*-os-*' all
exit

apache2 in ubuntu mission and httpd in redhat mission


conditionals:
apachenhttpd 6 to 17 run when os family is debian
18 to 28 run when os family is redhat

ansible -m setup -a "filter=*distriution*" all #checking facts
ansible -m setup -a "filter=*distriution*" -i hosts all
