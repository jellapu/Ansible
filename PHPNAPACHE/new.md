---
-name: Install apache2 and httpd
 hosts: all
 hosts: webserver
 become: yes
 tasks:
   - name: install apache2
     apt:
       name: paache2
       update_cache: yes
       stste: present
    when: ansible_facts['os_family'] == "Debian"
    