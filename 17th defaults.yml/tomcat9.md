---
ansible-playbook -i hosts --syntax-check tomcat9.yml
ansible-playbook -i hosts --check tomcat9.yml
ansible -m stat -a 'path=/opt/tomcat/;latest' all # will observer exist steps

Register: we know stucture and store the output


