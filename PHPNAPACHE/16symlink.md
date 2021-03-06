---
- name: install and configure tomcat 9
  hosts: appserver
  become: yes
  vars:
    java_package: openjdk-11-jdk
    tomcat_username: tomcat
    tomcat_home: /opt/tomcat
    tomcat_shell: /bin/false
    tomcat_version: '9.0.54'
    tomcat_service_dest: /etc/systemd/system/tomcat.service
  tasks:
    - name: update packages and install java
      apt:
        name: "{{ java_package }}"
        update_cache: yes
        state: present
    - name: add a tomcat user
      ansible.builtin.user:
        name: "{{ tomcat_username }}"
        home: "{{ tomcat_home }}"
        shell: "{{ tomcat_shell }}"
        state: present
    - name: download the tomcat distribution
      get_url:
        url: "https://archive.apache.org/dist/tomcat/tomcat-9/v{{ tomcat_version }}/bin/apache-tomcat-{{ tomcat_version }}.tar.gz"
        dest: "/tmp/apache-tomcat-{{ tomcat_version }}.tar.gz"
    - name: untar the tomcat distribution
      ansible.builtin.unarchive:
        src: "/tmp/apache-tomcat-{{ tomcat_version }}.tar.gz"
        dest: "{{ tomcat_home }}"
    - name: create a symlink
      ansible.builtin.file:
        src: "{{ tomcat_home }}/apache-tomcat-{{ tomcat_version }}"
        dest: "{{ tomcat_home }}/latest"
        state: link
    - name: give ownership to tomcat user and group
      ansible.builtin.file:
        path: "{{ tomcat_home }}"
        state: directory
        recurse: yes
        owner: "{{ tomcat_username }}"
        group: "{{ tomcat_username }}"
    - name: find all the shell files in the binaries
      find: 
        path: "{{ tomcat_home }}/latest/bin"
        pattern: "*.sh"
      register: shfiles
    - set_fact:
        tomcat_executables: "{{ shfiles.files | map(attribute='path') | list }}"
    - name: change permission of shell files
      file:
        path: "{{ item }}"
        mode: 0751
      with_items: "{{ tomcat_executables }}"
    - name: create tomcat service file
      ansible.builtin.copy:
        src: tomcat.service
        dest: "{{ tomcat_service_dest }}"
      notify:
        - reload and enable tomcat
    - name: ensure tomcat is running
      ansible.builtin.systemd:
        name: tomcat.service
        state: started
  handler:
    - name: reload and enable tomcat
      ansible.builtin.systemd:
        name: tomcat.service
        daemon_reload: yes
        enabled: yes
        state: reloaded 
